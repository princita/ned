# Break statement

The break statement is used to terminate the loop or statement in which it is present. After that, the control will pass to the statements that are present after the break statement, if available. If the break statement is present in the nested loop, then it terminates only those loops which contains break statement. 

# Continue statement

Continue is also a loop control statement just like the break statement.
continue statement is opposite to that of break statement, instead of
terminating the loop, it forces to execute the next iteration of the loop. As the
name suggests the continue statement forces the loop to continue or execute
the next iteration. When the continue statement is executed in the loop, the
code inside the loop following the continue statement will be skipped and the
next iteration of the loop will begin. 

# Pass statement

As the name suggests pass statement simply does nothing. The pass
statement in Python is used when a statement is required syntactically but you
do not want any command or code to execute. It is like null operation, as
nothing will happen is it is executed. Pass statement can also be used for
writing empty loops. Pass is also used for empty control statement, function
and classes. Syntax:

import pandas as pd

train_data=pd.read_csv("train.csv")

test_data=pd.read_csv("test.csv")


 <table>
    <thead>
      <tr>
        <th>Line Plot</th>
        <th>Dot Plot chart</th>
        <th>Creating Bars chart</th>
        <th>Scatter Plot</th>
        <th>Bar Plot</th>th
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)
plt.title(&quot;SALES&quot;)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)
plt.title(&quot;INCOME&quot;)

plt.show()</td>
            <td>
import matplotlib.pyplot as plt
import numpy as np

ypoints = train_data[&#39;Fare&#39;]

plt.plot(ypoints, linestyle = &#39;dotted&#39;)
plt.show()
</td>
            <td>
              import matplotlib.pyplot as plt

import numpy as np

x = np.array([&quot;A&quot;, &quot;B&quot;, &quot;C&quot;, &quot;D&quot;])

y = np.array([3, 8, 1, 10])

plt.bar(x,y)

plt.show()
</td>
       <td>
          
import matplotlib.pyplot as plt

import numpy as np

x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])

y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])

plt.scatter(x, y)

plt.show()
</td>
<td>
import matplotlib.pyplot as plt

import numpy as np


sb.barplot(x=&quot;Survived&quot;, y=&quot;Fare&quot;, data=train_data)

plt.show()
</td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td> </td>
           <td>
import matplotlib.pyplot as plt
import numpy as np
x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])
y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])
plt.scatter(x, y)
plt.show() </td>
            <td>
import matplotlib.pyplot as plt
import numpy as np
sb.barplot(x=&quot;Survived&quot;, y=&quot;Fare&quot;, data=train_data)
plt.show()
            </td>
        </tr>     
        <tr>
            <td></td>
            <td></td>
            <td> </td>
            <td>
import matplotlib.pyplot as plt
import numpy as np

sb.scatterplot(x=&quot;Age&quot;, y=&quot;Fare&quot;, data=train_data)
plt.show()
<td>
    </tbody>
  </table>


import seaborn as sns

a = sns.FacetGrid(train_data, hue = &#39;Survived&#39;, aspect=4 )

a.map(sns.kdeplot, &#39;Age&#39;, shade= True )

a.set(xlim=(0 , train_data[&#39;Age&#39;].max()))

a.add_legend()

print(&#39;Skew for train data:&#39;,train_data.Age.skew())

<table>
    <thead>
      <tr>
        <th>Histogram 1</th>
        <th> Histogram 2</th>
        <th>Histogram 3</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>
              fig, ax = plt.subplots()
ax.hist(train_data.Age, bins = 20)
ax.set_xlabel(&quot;Age&quot;)
ax.set_ylabel(&quot;Number of observations&quot;)
plt.show()</td>
            <td>null_ages = pd.isnull(train_data.Age)
known_ages = pd.notnull(train_data.Age)
preimputation = train_data.Age[known_ages]
sns.distplot(preimputation)
            </td>
            <td>import matplotlib.pyplot as plt
import numpy as np
import matplotlib.pyplot as pyplot

 bins=15
pyplot.rcParams[&quot;figure.figsize&quot;] = (10,10)

pyplot.hist(train_data[&quot;Fare&quot;], bins, alpha=1, label=&#39;train_data; orange Fare&#39;,

color=&#39;orange&#39;, weights = np.ones_like(train_data[&quot;Fare&quot;])/float(len(train_data[&quot;Fare&quot;])))

pyplot.hist(train_data[&quot;Age&quot;], bins, alpha=1, label=&#39;train_data; Age&#39;,

color=&#39;green&#39;, weights = np.ones_like(train_data[&quot;Age&quot;])/float(len(train_data[&quot;Age&quot;])))

pyplot.title(&#39;Fare/Age&#39;)

pyplot.xlabel(&#39;Age&#39;)

pyplot.ylabel(&#39;Percent&#39;)

pyplot.legend(loc=&#39;upper right&#39;)

pyplot.show()
            </td>
        </tr>
        <tr>
            <td>Vision</td>
            <td>KNN</td>
            <td>Time Series Forecasts</td>
        </tr>
    </tbody>
  </table>


