# Corsi Task

An OpenSesame implementation of the Corsi Block-Tapping Task, using OSWeb for browser-based administration. The task is designed to assess visuospatial short-term memory.

## Task Description

Participants are presented with a set of blocks on the screen that are highlighted in a sequence. The objective is to remember the sequence and reproduce it by selecting the blocks in the same order.

The task assesses the participant's ability to retain and recall spatial sequences.

## Language

The experiment instructions are in Swedish.

## Implementation

The experiment is developed in OpenSesame and uses OSWeb for execution in a web browser.

## Configuration

The task uses an adaptive sequence length progression, starting with two blocks and increasing to a maximum of ten blocks.

Each sequence length is presented twice. If the participant fails to correctly reproduce both sequences of the same length, the task terminates.

| Sequence Length | Number of Trials |
|-----------------|------------------|
| 2               | 2                |
| 3               | 2                |
| 4               | 2                |
| 5               | 2                |
| 6               | 2                |
| 7               | 2                |
| 8               | 2                |
| 9               | 2                |
| 10              | 2                |

## Participant Identification

The experiment is designed to run through JATOS and retrieves the participant ID (`pid`) from the URL query parameters.

```javascript
vars.ID = jatos.urlQueryParameters.pid;
```

For example, if the experiment is launched with:

`https://example.com/study?pid=1234`

Then `vars.ID` will contain `"1234"`.

When running the experiment without JATOS, the reference to `jatos.urlQueryParameters` should be removed or replaced to avoid errors.
