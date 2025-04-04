# ottr-preview

A repository for the composite action to render previews. 

## How to use: 

You can make a preview like this for an Rmd website or course that is set up for bookdown: 
```
steps:
    - name: Checkout Actions Repository
      uses: actions/checkout@v4
      with:
        fetch-depth: 0

    - name: Run render for Rmd
      uses: ottrproject/ottr-preview@cansavvy-patch-1
      with:
        toggle_website: "rmd"
        root_path: test-rmd
```

You can make a preview like this for an Quarto website or course that is set up for quarto: 
```
steps:
    - name: Checkout Actions Repository
      uses: actions/checkout@v4
      with:
        fetch-depth: 0

    - name: Run render for Rmd
      uses: ottrproject/ottr-preview@cansavvy-patch-1
      with:
        toggle_website: "quarto"
        root_path: test-quarto
```
