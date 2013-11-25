---
layout: post
title: "Hbase SubstringComparator"
date: 2013-11-25 23:07:17 +0800
comments: true
categories: 
---
One of the hbase scan usage, to filter the rows whose key has a specific substring

The docs link [Hbase SubstringComparator](http://hbase.apache.org/apidocs/org/apache/hadoop/hbase/filter/SubstringComparator.html)
``` sh
>import org.apache.hadoop.hbase.filter.CompareFilter
>import org.apache.hadoop.hbase.filter.SubstringComparator
>scan 'YOUR_TABLE_NAME', {FILTER => org.apache.hadoop.hbase.filter.RowFilter.new(CompareFilter::CompareOp.valueOf('EQUAL'),SubstringComparator.new("substring_in_key"))}
```
