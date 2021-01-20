
# Phase 1 Code Challenge Review

![let's do this](https://media.giphy.com/media/BpGWitbFZflfSUYuZ9/giphy.gif)

The topics covered will be:

  - [Interacting with Pandas dataframes](#dataframes)
  - [Visualization](#viz)
  - [Python Data Structures](#datastructures)
    


```python
# Import pandas, numpy, matplotlib, pickle, json
```

<a id='dataframes'></a>
# DataFrames

To practice working with dataframes, we will use some Facebook data taken from the UCI Machine Learning repository.

Refer to this paper if you are interested in learning more. There is also a nice description of the features: http://www.math-evry.cnrs.fr/_media/members/aguilloux/enseignements/m1mint/moro2016.pdf



# Task 1

Read 'dataset_Facebook.csv' from data/Facebook_metrics into the notebook as a Pandas dataframe.


```python
# Your code here
facebook = None
```

# Task 2

### 2a: Count how many na's there are in each column
 


```python
# Your code here
```

### 2b: Drop records that have na's in any column without altering the dataframe in memory
 


```python
# Your code here
```

### 2c: Drop records that have na's in the `share` column while altering the dataframe in memory


```python
# Your code here
```

# Task 3

An impression is each time a post is displayed.  

Create a new column called `likes_per_impression` which divides the number of comments per post by the number of likes per post.


```python
# Your code here
```

# Task 4

Locate the `record` of a **Photo** that has the largest value in the `like` column


```python
# Your code here
```

# Task 5
What is the mean number of Total Interactions for photos?


```python
mean_interactions_photos = None
```

<a id='viz'></a>
# Visualization

# Task 6

Create a bar chart showing the number of posts per month.
Order the x-axis by month as they appear on the calendar.
Don't forget to add labels and a title.  

Use the `plt.subplot` method if you can, but if you can't, resort to the `plt` syntax.


```python

```

# Task 7

Create a scatter plot that shows the correlation between total interactions and likes.


```python
# Your code here
```

<a id='datastructures'></a>
# Data Structures

For this next section, we will explore a nested dictionary that comes from the Spotify API.  

The `data` variable below contains 6 separate pings, each of which returns a list of the top 20 songs streamed on a given day.



```python
with open('data/offset_newreleases.p','rb') as read_file:
    responses = pickle.load(read_file)
```


```python
data = [json.loads(r) for r in responses]
```


```python
len(data)
```




    6



We will work only with the first response.


```python
first_response = data[0]
```

# Task 8

Explore the `first_response` dictionary and find how to access the list of twenty songs.
Assign the list to the variable `first_twenty_songs`.
Hint: print out the keys at each level with .keys().


```python
# Your code here
first_twenty_songs = None
```

# Task 9

Create a list of **track names** of all twenty songs using a for loop or list comprehension.


```python
track_names = []

# Your code here
```

# Task 10

Create a dictionary called `song_dicitonary` which consists of each track name `string` as a key and a `list` of artists associated with each track as a value.

# Task 11

Create a function with takes an **artist name** and the **song_dictionary** as arguments, and returns a `list` of songs written by that artist. 


```python
# Your code here
def find_songs_by_artist():
    
    '''
    Parameters:
    arist_name: a string of an artist's name to be used to search the dictionary
    song_dictionary:  a dictionary of top_twenty songs with song name as keys and a list of 
    artist names as values
    
    Returns:
    A list of songs which the given artist appeared on
    '''
```


```python
find_song_by_artist('Selena Gomez', song_dictionary)
```




    ['Ice Cream (with Selena Gomez)']


