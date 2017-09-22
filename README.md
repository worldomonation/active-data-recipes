# active-data-recipes

A repository of various ActiveData recipes. A recipe is a small snippet that runs one or more active
data queries and returns the output. Queries can sometimes be modified by command line arguments and
output can sometimes be post-processed.

Each recipe should try to answer a single question.

# Installation

    pip install active-data-recipes

# Usage

Run:

    adr <recipe> <options>

For a list of recipes:

    adr --list

For recipe specific options see:

    adr <recipe> -- --help

# Recipes

## Hours on Try

    adr hours_on_try

Returns the total number of compute hours spent on try over the past week. The date range can be
modified with `--from` and `--to` using the format described [here][0]. For example:

    adr hours_on_try --from today-2month --to today-month

## Try Usage

    adr try_usage

Prints stats on what percentage of try pushes are being scheduled with various different mechanisms
over the last week. The date range can be modified the same as the `hours_on_try` recipe.

[0]: https://github.com/klahnakoski/ActiveData/blob/dev/docs/jx_time.md
