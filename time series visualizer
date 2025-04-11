import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
from pandas.plotting import register_matplotlib_convertors
register_matplotlib_convertors()

#import data (make sure to parse dates, consider setting index column to "dates".)
df = pd.read.csv("fcc-forum-pageviews.csv" ,parse_dates = ["dates"], index_col="date")

# clean data
df = df[
    (df["value"]  >= df["value"].quantile(0.025)) &
    (df["value"]  <= df["value"].quantile(0.975))]


def deaw_line_plot():
    #draw line plot
    fig, ax = plt.subplots(figsize=(10,5))
    ax.plot(df.index, df["value"], "r", linewidth=1)

    ax.set_title("daily freecodecamp forum page views 5/2016-12/2019")
    ax.set_xlabel("date")
    ax.set_ylabel("page views")

    # save image and return fig ( don"t change this part )
    fig.savefig("line_plot.png")
    return fig

def draw_bar_plot():
    #copy and modify data for monthly bar plot
    df["month"] = df.index.month
    df["year"] = df.index.year
    df_bar = 
    df_bar = 

    # draw bar plot
    fig = df_bar.plot.bar(legend=true, figsize= (13,6), ylabel="average page views", xlabel="years").figure
    plt.legend([ "january", "february", "march", "april", "may", "june", "july", august", "september", "october", "november", "december])

    plt.xticks(fontsize = 8)
    plt.yticks(fontsize = 8)
   
    #save image and return fig ( don"t change this part)
    fig.savefig("bar_plot.png")
    return_fig

def draw_bar_plot():
    # prepare data for box plots (this part is done)
    df_box =df.copy()
    df_box.reset_index(inplace=true)
    df_box["year"] = [d.year for d in df_box.date ]
    df_box["month"] = [d.strftime("%b" for d in df_box.date)]
    
    #draw box plots (using seaborn)

   fig,axes= plt.subplots(nrows=1, ncols=2, figsize=(10,5))
   axes[0] = sns.boxplot(x=df_box["year"], y=df_box["value"], ax = axes[0])
   axes[1] = sns.boxplot(x=df_box["month"], y=df_box["value"], ax = axes[1])
 
   axes[0].set_title("year-wise boxplot (trend)")
   axes[0].set_xlabel("year")
   axes[0].set_ylabel("page views")
 
   axes[1].set_title("month-wise boxplot (seasonality")")
   axes[1].set_xlabel("month")
   axes[1].set_ylabel("page views")


     #save image and return fig (don"t change this part)
     fig.savefig( "bar_plot.png")
     return fig
