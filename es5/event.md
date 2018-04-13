##事件{#es5-event}
- 【**强制**】当给事件附加数据时（无论是 DOM 事件还是私有事件），传入一个哈希而不是原始值。这样可以让后面的贡献者增加更多数据到事件数据而无需找出并更新事件的每一个处理器。

  ```js
  // bad
  $(this).trigger('listingUpdated', listing.id);
  $(this).on('listingUpdated', function (e, listingId) {
    // do something with listingId
  });
  
  // good
  $(this).trigger('listingUpdated', { listingId : listing.id });
  $(this).on('listingUpdated', function (e, data) {
    // do something with data.listingId
  });
  ```