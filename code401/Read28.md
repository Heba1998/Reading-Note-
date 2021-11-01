#  RecyclerView


![](https://i.ytimg.com/vi/UCddGYMQJCo/maxresdefault.jpg)


## **Create dynamic lists with RecyclerView**


![](https://external-preview.redd.it/aHBjzQQXYF4U26ZDpkbw8IZeU-6cJCoRdv7JZM3xZoc.jpg?auto=webp&s=a3dea686120dc581bcfed40707e4bfcba2dcabfc)

- RecyclerView makes it easy to efficiently display large sets of data. You supply the data and define how each item looks, and the RecyclerView library dynamically creates the elements when they're needed.
- It is a container for displaying large datasets which can be scrolled efficiently by maintaining limited number of views.
- It is more flexible and advanced version of GridView and ListView.
- RecyclerView reuses the view for new items that have scrolled onscreen.

### Key classes

Several different classes work together to build your dynamic list.

- ViewGroup
- RecyclerView.ViewHolder
- RecyclerView.Adapter
- LayoutManager

### Steps for implementing your RecyclerView

If you're going to use RecyclerView, there are a few things you need to do:

1. First of all, decide what the list or grid is going to look like. Ordinarily you'll be able to use one of the RecyclerView library's standard layout managers.

2. Design how each element in the list is going to look and behave. Based on this design, extend the ViewHolder class. Your version of ViewHolder provides all the functionality for your list items. Your view holder is a wrapper around a View, and that view is managed by RecyclerView.

3. Define the Adapter that associates your data with the ViewHolder views.

### Plan your layout

- The items in RecyclerView are arranged by a LayoutManager class.
- The RecyclerView library provides three layout managers.

1. LinearLayoutManager arranges the items in a one-dimensional list.
2. GridLayoutManager arranges all items in a two-dimensional grid (Vertically and Horizantaly)
3. StaggeredGridLayoutManager: it does not require that items in a row have the same height or items in the same column have the same width.

### Implementing your adapter and view holder:
  - When you define your adapter, you need to override three key methods:
    - `onCreateViewHolder()` RecyclerView calls this method whenever it needs to create a new ViewHolder.

    - `onBindViewHolder()` RecyclerView calls this method to associate a ViewHolder with data.

    - `getItemCount()`RecyclerView calls this method to get the size of the data set.