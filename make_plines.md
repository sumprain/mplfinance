## Steps for adding plines

### What will it do?

It will draw tline between two dates.

It will calculate the slope of the tline.

It will draw a line parallel to the tline through a given date.

  kwargs to be used:
  
    pline_use: open, high, low or close or an average of any combination.
    extend_start and extend_end: dates offsetted before the date point and after 
    the date point.
    
### Usage

```{python}
import mplfinance as mf

dates_plines = [(('2021-01-01', '2021-01-10'), '2021-01-05'), 
                (('2022-01-01', '2022-03-10'), '2022-02-10'), ]
              
mf.plot(..., plines = [dict(plines = dates_plines, pline_use = (('low', ), ('high', )),
                                                   colors = ('r', 'b'),
                                                   kwarg = ('value_tline', 'value_pline'),), 
                       dict(plines = dates_plines, ...)
                       ], ...)

```
