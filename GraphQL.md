#  Django GraphQL

Instruction for setting up GraphQL in a Django project.

[Graphene documentation](https://docs.graphene-python.org/en/latest/)

**Table of Contect:**

1. [why Graphql?](#why-graphql)
1. [Graphene Installation](#graphene-installtion)
1. [Creating Schemas](#creating-schemas)
1. Using Graphiql
1. [Roadmap](#roadmap)
1. [Foot Note](#foot-note)
1. [Footer](#footer)

## why Graphql?

- Get only data that you want 
- easier to manage endpoint

## Graphene Installation

Install  Graphene: `pip install django_graphene`

## Creating Schemas
```py
import graphene
from graphene_django import DjangoObjectType

from .models import Hero

class HeroType(DjangoObjectType):
    class Meta:
        model = Hero

class Query(graphene.ObjectType):
    heroes = graphene.List(HeroType)

    def resolve_heroes(self, info, **kwargs):
        return Hero.objects.all()
```

---

| light color  | Current State | Next State |
|:------- | :------- | :------- |
| Green | Green | Yellow |
| Yellow | Yellow | Red |

<details>
<summary> Section Header </summary>


Section body text.
- Hello
- test


</details>


## Foot Note
Happy tree are happy. [^1]

## Footer
[^1]: By Bob Ross
