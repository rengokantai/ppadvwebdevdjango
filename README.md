# ppadvwebdevdjango

## Extendning Class Based Views
```
ListView
DetailView
DeleteView
```
```
from django.views import generic
from .models import Question

class IndexView(generic.ListView):
  template_name=
  context_object_name=
  def get_queryset(self):
    return Question.objects.order_by
```


```
class DetailView(generic.DetailView):
  model = Question
  template_name = 'polls/detail.html'
class DeleteView(generic.DeleteView):
  model = Question
  success_url = "/polls/"
```

### Using Mixins
#### What is MRO
- python's way of figuring out what method should be called
