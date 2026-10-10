
import { useEffect, useRef, useState } from "react";

export function useTelemetry() {
  const [telemetry, setTelemetry] = useState({
    mouseVelocity: 0,
    clickCount: 0,
    hesitationTime: 0
  });

  const lastPosition = useRef({
    x: 0,
    y: 0,
    time: Date.now()
  });

  const lastMovementTime = useRef(Date.now());

  useEffect(() => {
    const handleMouseMove = (event) => {
      const now = Date.now();
      const previous = lastPosition.current;

      const dx = event.clientX - previous.x;
      const dy = event.clientY - previous.y;
      const elapsed = now - previous.time;

      const distance = Math.sqrt(dx * dx + dy * dy);
      const velocity =
        elapsed > 0 ? distance / elapsed : 0;

      setTelemetry((old) => ({
        ...old,
        mouseVelocity: Number(velocity.toFixed(2))
      }));

      lastPosition.current = {
        x: event.clientX,
        y: event.clientY,
        time: now
      };

      lastMovementTime.current = now;
    };

    const handleClick = () => {
      const hesitation =
        Date.now() - lastMovementTime.current;

      setTelemetry((old) => ({
        ...old,
        clickCount: old.clickCount + 1,
        hesitationTime: hesitation
      }));
    };

    window.addEventListener("mousemove", handleMouseMove);
    window.addEventListener("click", handleClick);

    return () => {
      window.removeEventListener("mousemove", handleMouseMove);
      window.removeEventListener("click", handleClick);
    };
  }, []);

  return telemetry;
}




# Day 7 – AuraGen Telemetry Tracker

## Objective
Build the initial user interaction tracking module for AuraGen.

## Work Completed
- Created a React custom hook.
- Tracked mouse movement.
- Calculated approximate mouse velocity.
- Counted user clicks.
- Recorded time since the last mouse movement.
- Displayed telemetry values in the interface.

## Technologies Used
- React
- JavaScript
- React Hooks

## Project Relevance
This module is an initial step toward the AuraGen
Friction Engine, which uses interaction telemetry
to help identify potential user frustration.

## Limitations
This version does not yet calculate a Cognitive Load
Score, detect erroneous clicks, or stream events through
WebSockets.

## Next Step
Develop a Cognitive Load Score calculation.

## Status
Initial telemetry tracker created.

