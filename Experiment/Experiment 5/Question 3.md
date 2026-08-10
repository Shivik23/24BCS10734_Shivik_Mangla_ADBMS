# Conditional Statements in PostgreSQL (PL/pgSQL)

## 1. IF THEN

```sql
DO $$
DECLARE
    AGE INT := 19;

BEGIN
    IF AGE >= 18 THEN
        RAISE NOTICE 'Your age is % and you are eligible to vote', AGE;
    END IF;

    RAISE NOTICE 'You are inside begin end block';
END;
$$;
```

---

## 2. IF ELSE

```sql
DO $$
DECLARE
    AGE INT := 17;

BEGIN
    IF AGE >= 18 THEN
        RAISE NOTICE 'Your age is % and you are eligible to vote', AGE;
    ELSE
        RAISE NOTICE 'Your age is % and you are not eligible to vote', AGE;
    END IF;

    RAISE NOTICE 'You are inside begin end block';
END;
$$;
```

---

## 3. IF ELSIF ELSE

```sql
DO $$
DECLARE
    VAL INT := 17;

BEGIN
    IF VAL >= 0 AND VAL <= 10 THEN
        RAISE NOTICE 'Value is % and in range between 1 to 10', VAL;

    ELSIF VAL > 10 AND VAL <= 20 THEN
        RAISE NOTICE 'Value is % and in range between 11 to 20', VAL;

    ELSE
        RAISE NOTICE 'Value is % and is greater than 20', VAL;
    END IF;

    RAISE NOTICE 'You are inside begin end block';
END;
$$;
```
