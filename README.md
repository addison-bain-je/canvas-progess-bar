# canvas-progess-bar
Loading progress bar for Canvas App

Progress bar to show user that a loading process is in-progress.
A good example is if you are loading multiple data sources (e.g. SP lists) into Collections, and it is useful to inform the user that some waiting time is to be expected.

With modern controls enabled in canvas app, you can use the Progress Bar control and make some modifications to the control properties to achieve a similar result.

![](https://github.com/addison-bain-je/canvas-progess-bar/blob/main/progress_bar.gif)


OnSelect of the "Load Data" button:
```
UpdateContext({
   locLoadingMessage: "Loading Batch 1 of 5",
   locLoadingPercent: 0.2
});
ClearCollect(
            col01, 'SharePointList1'
);

UpdateContext({
   locLoadingMessage: "Loading Batch 2 of 5",
   locLoadingPercent: 0.4
});
ClearCollect(
            col02, 'SharePointList2'
);

UpdateContext({
   locLoadingMessage: "Loading Batch 3 of 5",
   locLoadingPercent: 0.6
});
ClearCollect(
            col03, 'SharePointList3'
);

UpdateContext({
   locLoadingMessage: "Loading Batch 4 of 5",
   locLoadingPercent: 0.8
});
ClearCollect(
            col04, 'SharePointList4'
);

UpdateContext({
   locLoadingMessage: "Loading Batch 5 of 5",
   locLoadingPercent: 1.0
});
ClearCollect(
            col05, 'SharePointList5'
);


UpdateContext({
    locLoadingMessage: "Loading Completed",
    locLoadingPercent: 1.0
});
ClearCollect(
        colEmps,
        col01,
        col02
        col03,
        col04,
        col05
);

```

For the Progress Bar control

Value property:
```
locLoadingPercent
```
Max
```
1
```
