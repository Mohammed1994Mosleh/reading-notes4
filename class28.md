# class28 Reading Notes:Create dynamic lists with RecyclerView   

* RecyclerView facilitates display large sets of data. 
![RecyclerView ](https://res.cloudinary.com/practicaldev/image/fetch/s--MUx-LV8y--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/4h2wjwo0dlzkenw9ewnm.png)


* RecyclerView reuses the view for new items that have scrolled onscreen ,when item scolls off screen.

#### Advanteges of RecyclerView :

1. improves performance
2. improving your app's responsiveness
3. reducing power consumption.

### Key classes:

* Their is different classes work together to build your dynamic list:

- RecyclerView
   
   * contains the views corresponding to your data. 

-  RecyclerView.ViewHolder.

   * After the view holder is created, the RecyclerView binds it to its data.

- RecyclerView.Adapter.
  
  *  requests those views, and binds the views to their data, by calling methods in the adapter.

- LayoutManager :

* arranges the individual elements in your list.

### Steps for implementing your RecyclerView:

- before start ,should decide and answer the following:

1. what the list or grid is going to look like

2. Design how each element in the list is going to look and behave.

3. Define the Adapter that associates your data with the ViewHolder views.

#### Plan your layout:

   - Types of layout managers:
     
     1. LinearLayoutManager arranges the items in a one-dimensional list.
     
     2. GridLayoutManager arranges all items in a two-dimensional grid

     3. StaggeredGridLayoutManager

#### Implementing your adapter and view holder:

- At this stage the main two thing is Adapter and ViewHolder.

- Three key method of Adapter :

   1. onCreateViewHolder(): to create a new ViewHolder
   
   2. onBindViewHolder():fetches the appropriate data and uses the data to fill in the view holder's layout

   3. getItemCount(): o get the size of the data set