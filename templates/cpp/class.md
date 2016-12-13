<a id="{{id}}"></a>
# {{kind}} `{{name}}`

{{#if basecompoundref}}
```
{{kind}} {{name}}
  {{#each basecompoundref}}
  : {{prot}} {{name}}
  {{/each}}
```  
{{/if}}

{{briefdescription}}

{{detaileddescription}}

## 摘要

| 成员                        | 描述                                |
|--------------------------------|---------------------------------------------|
{{#each filtered.compounds}}
| {{cell proto}}                 | {{cell briefdescription}}                   |
{{/each}}
{{#each filtered.members}}
| {{cell proto}}                 | {{cell briefdescription}}                   |
{{/each}}

## 成员

{{#each filtered.compounds}}
{{#if id}}
<a id="{{id}}"></a>
{{/if}}
### {{title proto}}

{{briefdescription}}

{{detaileddescription}}
{{/each}}

{{#each filtered.members}}
{{#if id}}
<a id="{{id}}"></a>
{{/if}}
### {{title proto}}

{{briefdescription}}

{{detaileddescription}}

{{/each}}



---

## 摘要

| 成员                        | 描述                                |
|--------------------------------|---------------------------------------------|
{{#each compounds}}
| {{kind}}                 | {{name}}                   |
{{/each}}


{{#each members}}
{{#eq 'enum' kind}}

## 枚举 ```{{name}}```
{{/eq}}
{{#eq 'enumvalue' kind}}
>#### {{name}}
{{/eq}}
{{/each}}

----
