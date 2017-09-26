# profile-manager

A Polymer Element that managers user profiles saved in elasticsearch.

### Example
```js
var buildSearchStateFunction = function(searchParameters) {
  return {
    field1: searchParameters.field1 || [],
    field2: searchParameters.field2 || []
  };
};

var queryBuilderCallback = {
  dates: function(list) {
    return list;
  },
  terms: function(list) {
    return list;
  }
};

var queryBuilderConfig = {
  field1: {
    field: 'testField1'
  },
  field2: {
    field: 'testField2'
  }
};

var searchParameters = {
  field1: ['value1'],
  field2: ['value2', 'value3', 'value4']
};
```

```html
<profile-manager
  build-search-state-function="[[buildSearchStateFunction]]"
  client="[[client]]"
  index-name="dig-profiles"
  index-type="profile"
  query-builder-callback="[[queryBuilderCallback]]"
  query-builder-config="[[queryBuilderConfig]]"
  search-parameters="[[searchParameters]]"
  username="user-1234"
  blur-images="{{blurImages}}"
  cases="{{cases}}"
  email-address="{{emailAddress}}"
  notifications="{{notifications}}"
  notification-interval="{{notificationInterval}}"
  profile-manager="{{profileManager}}"
  user-id="{{userId}}"
  user-loading="{{userLoading}}">
</profile-manager>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

