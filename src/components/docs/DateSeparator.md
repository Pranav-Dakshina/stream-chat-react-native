The date separator between messages.
Here's what it looks like for today.

```js
const date = new Date();
<React.Fragment>
  <DateSeparator message={{ date }} />
  <DateSeparator message={{ date }} alignment="center" />
  <DateSeparator message={{ date }} alignment="left" />
</React.Fragment>;
```

and for a date in the past:

```js
const date = new Date('December 17, 1995 03:24:00');
<React.Fragment>
  <DateSeparator message={{ date }} />
  <DateSeparator message={{ date }} alignment="center" />
  <DateSeparator message={{ date }} alignment="left" />
</React.Fragment>;
```

and adding custom date formatting:

```js
const date = new Date('December 17, 1995 03:24:00');

function formatDate(d) {
  return <h2>Messages posted after {d.toDateString()}</h2>;
}

<React.Fragment>
  <DateSeparator formatDate={formatDate} message={{ date }} />
  <DateSeparator
    formatDate={formatDate}
    message={{ date }}
    alignment="center"
  />
  <DateSeparator formatDate={formatDate} message={{ date }} alignment="left" />
</React.Fragment>;
```
