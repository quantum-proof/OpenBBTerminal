.. role:: python(code)
    :language: python
    :class: highlight

|

.. raw:: html

    <h3>
    > Getting data
    </h3>

{{< highlight python >}}
portfolio.metric.rsquare(
    portfolio_engine: openbb_terminal.portfolio.portfolio_engine.PortfolioEngine,
    chart: bool = False,
) -> pandas.core.frame.DataFrame
{{< /highlight >}}

.. raw:: html

    <p>
    Get R2 Score for portfolio and benchmark selected
    </p>

* **Parameters**

    portfolio_engine: PortfolioEngine
        PortfolioEngine class instance, this will hold transactions and perform calculations.
        Use `portfolio.load` to create a PortfolioEngine.

* **Returns**

    pd.DataFrame
        DataFrame with R2 Score between portfolio and benchmark for different periods

* **Examples**

    {{< highlight python >}}
    >>> from openbb_terminal.sdk import openbb
    >>> p = openbb.portfolio.load("openbb_terminal/miscellaneous/portfolio_examples/holdings/example.csv")
    >>> output = openbb.portfolio.metric.rsquare(p)
    {{< /highlight >}}
