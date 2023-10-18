
```
return HttpResponseRedirect(reverse("polls:results", args=(question.id,)))
```

We are using the reverse() function in the HttpResponseRedirect constructor in this example. This function helps avoid having to hardcode a URL in the view function. It is given the name of the view that we want to pass control to and the variable portion of the URL pattern that points to that view. In this case, using the URLconf we set up in Tutorial 3, this reverse() call will return a string like

> "/polls/3/results/"
where the 3 is the value of question.id. This redirected URL will then call the 'results' view to display the final page.