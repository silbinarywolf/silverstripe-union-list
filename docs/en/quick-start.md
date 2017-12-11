# Quick Start

1. Install via composer and run dev/build.

2. Example:
```
$promotedItems = Page::get()->filter('IsPromoted', 1)->limit(3);
$regularItemsList = Page::get()->filter('IsPromoted', 0);
$list = UnionList::create(array(
    $promotedItems,
    $regularItemsList,
));
$list = $list->limit(20);
```
