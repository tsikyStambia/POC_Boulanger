<?xml version="1.0" encoding="UTF-8"?>
<md:node xmlns:md="http://www.stambia.com/md" defType="com.stambia.function.folder" id="_h4LpMCtZEeyq-96bFbiw2A" name="boulangerFunctions" md:ref="resource.md#UUID_MD_UDF?fileId=UUID_MD_UDF$type=md$name=User%20Defined%20Functions?" internalVersion="v1.0.0">
  <attribute defType="com.stambia.function.folder.prefix" id="_oS-iYCtZEeyq-96bFbiw2A" value="bf"/>
  <node defType="com.stambia.function.function" id="_olJQcCtZEeyq-96bFbiw2A" name="num_with_comma">
    <node defType="com.stambia.function.parameter" id="_pIIBsCtZEeyq-96bFbiw2A" name="string"/>
    <node defType="com.stambia.function.parameter" id="_s3BVUCtZEeyq-96bFbiw2A" name="scale"/>
    <node defType="com.stambia.function.parameter" id="_t_WPUCtZEeyq-96bFbiw2A" name="precision"/>
    <node defType="com.stambia.function.implementation" id="_u4W68StZEeyq-96bFbiw2A" name="4snow">
      <attribute defType="com.stambia.function.implementation.expression" id="_1nN_oCtZEeyq-96bFbiw2A" value="to_number(replace($string, ',', '.'), $scale, $precision)"/>
      <attribute defType="com.stambia.function.implementation.productCode" id="_2RDm0CtZEeyq-96bFbiw2A">
        <values>REDSHIFT</values>
        <values>SNOWFLAKE</values>
      </attribute>
    </node>
    <node defType="com.stambia.function.implementation" id="_6zbl0StZEeyq-96bFbiw2A" name="4ora">
      <attribute defType="com.stambia.function.implementation.productCode" id="_8XW2sCtZEeyq-96bFbiw2A">
        <values>ORACLE</values>
      </attribute>
      <attribute defType="com.stambia.function.implementation.expression" id="_ADZqoCtaEeyq-96bFbiw2A" value="to_numeric(replace($string, ',', '.'), $precision, $scale)"/>
    </node>
  </node>
</md:node>