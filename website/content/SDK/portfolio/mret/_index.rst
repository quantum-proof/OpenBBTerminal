.. role:: python(code)
    :language: python
    :class: highlight

|

To obtain charts, make sure to add :python:`chart = True` as the last parameter.

.. raw:: html

    <h3>
    > Getting data
    </h3>

{{< highlight python >}}
portfolio.mret(
    portfolio_engine: openbb_terminal.portfolio.portfolio_engine.PortfolioEngine,
    window: str = 'all',
    chart: bool = False,
) -> pandas.core.frame.DataFrame
{{< /highlight >}}

.. raw:: html

    <p>
    Get monthly returns
    </p>

* **Parameters**

    portfolio_engine: PortfolioEngine
        PortfolioEngine class instance, this will hold transactions and perform calculations.
        Use `portfolio.load` to create a PortfolioEngine.
    window : str
        interval to compare cumulative returns and benchmark
    chart: bool
       Flag to display chart


* **Returns**

    pd.DataFrame
        DataFrame with monthly returns

* **Examples**

    {{< highlight python >}}
    >>> from openbb_terminal.sdk import openbb
    >>> p = openbb.portfolio.load("openbb_terminal/miscellaneous/portfolio_examples/holdings/example.csv")
    >>> output = openbb.portfolio.mret(p)
    {{< /highlight >}}

|

.. raw:: html

    <h3>
    > Getting charts
    </h3>

{{< highlight python >}}
portfolio.mret(
    portfolio_engine: openbb_terminal.portfolio.portfolio_engine.PortfolioEngine,
    window: str = 'all',
    raw: bool = False,
    show_vals: bool = False,
    export: str = '',
    external_axes: Optional[matplotlib.axes._axes.Axes] = None,
    chart: bool = False,
)
{{< /highlight >}}

.. raw:: html

    <p>
    Display monthly returns
    </p>

* **Parameters**

    portfolio_engine: PortfolioEngine
        PortfolioEngine class instance, this will hold transactions and perform calculations.
        Use `portfolio.load` to create a PortfolioEngine.
    window : str
        interval to compare cumulative returns and benchmark
    raw : False
        Display raw data from cumulative return
    show_vals : False
        Show values on heatmap
    export : str
        Export certain type of data
    external_axes: plt.Axes
        Optional axes to display plot on
    chart: bool
       Flag to display chart

