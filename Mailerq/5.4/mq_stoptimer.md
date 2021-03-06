# Function MQ_stopTimer

This function stops a timer that was previously created. Note that this function should only be called to stop a timer that has not yet fired yet, because a timer will automatically be cleaned up and calling MQ_stopTimer after this is not legal.

```c
/**
 *  Stop a timer before it expires
 *
 *  @param  timer   the timer to stop
 */
void MQ_stopTimer(MQ_Timer *timer);

```

For a detailed example, see [MQ_startTimer](mq_starttimer)
