
# RecyclerView
It is ui component which allows us to create a scrolling list. It is basically a new ViewGroup used to render any adapter-based view in horizontal/vertical /grid or staggered grid manner using the Viewholder pattern

![0_TLiq0cEJRZbWaUET](https://user-images.githubusercontent.com/18142767/212524660-1d57147e-9f99-4990-bcf6-609b2e1b62e8.gif)

- **RecyclerView.Adapter:** Provides a binding from data set to item views that are displayed within the RecyclerView. The adapter knows how to associate each item-view position in the RecyclerView to a specific location in the data source.

- **RecyclerView.LayoutManager:** help to decide how list item are being displayed like vertical, horizontal, grid or staggered.

- **RecyclerView.ViewHolder:** It is mandatory to use with recyclerView and helps us to draw the UI for individual items that we want to draw on the screen.

![recycle-view](https://miro.medium.com/max/828/1*sdn9nN70HULW-8W7j1_C6Q.webp)

When a view scrolls out of sight and is no longer displayed, it becomes a scrap view.
The Recycler has a Scrap Heap Caching System for scrap views

**Scrap Heap:** It is a lightweight collection where views can be returned to the Layout Manager directly without passing the view back to Adapter again. This is because the data is still attached to the ViewHolder. So no need to pass it back to the Adapter for binding the data.

**Recycle Pool:** It is a collection which consists of views that are assumed to have incorrect data (data from a different position or index) also called the dirty view, is always passed to the adapter back so that data can be attached or bound again to the ViewHolder and then returned to the Layout Manager.

**Reference**
   1. https://proandroiddev.com/recycler-view-internals-i-birth-of-viewholder-ae536760839c
   2. https://medium.com/1mgofficial/how-recyclerview-works-internally-71290de5d2c4
