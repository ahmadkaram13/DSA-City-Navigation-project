# Pseudocode — City Navigation System

## Undo Step — Muaaz Ch.

FUNCTION undoStep(stack):
    IF stack empty:
        PRINT "No previous steps."
        RETURN null
    END IF

    last = stack.pop()
    RETURN last
END FUNCTION
