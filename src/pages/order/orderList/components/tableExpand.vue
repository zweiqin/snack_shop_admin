<template>
    <div class="expand">
        <Row class="expand-row">
            <Col span="8">
                <span class="expand-key">商品总价：</span>
                <span class="expand-value" v-text="row.total_price"></span>
            </Col>
            <Col span="8">
                <span class="expand-key">下单时间：</span>
                <span class="expand-value" v-text="row.add_time"></span>
            </Col>
            <Col span="8">
                <span class="expand-key">推广人：</span>
                <span class="expand-value" v-text="row.spread_nickname?row.spread_nickname:'无'"></span>
            </Col>
        </Row>
      <Row class="expand-row">
        <Col span="8">
          <span class="expand-key">用户备注：</span>
          <span class="expand-value" v-text="row.mark?row.mark:'无'"></span>
        </Col>
        <Col span="8">
          <span class="expand-key">商家备注：</span>
          <span class="expand-value" v-text="row.remark?row.remark:'无'"></span>
        </Col>
        <Col span="8">
          <span class="expand-key">核销码：</span>
          <span class="expand-value" v-text="row.verify_code?row.verify_code:'无'"></span>
        </Col>
      </Row>
      <Row v-if="row.shipping_type==1">
        <Col span="8">
          <span class="expand-key">配送时间：</span>
          <span class="expand-value" v-text="row.deliveryTime?row.deliveryTime:'无'"></span>
        </Col>
      </Row>
    </div>
</template>

<script>
    export default {
        name: 'table-expand',
        props: {
            row: Object
        }
    }
</script>

<style scoped>
    .expand{
        padding-left: 50px;
    }
    .expand-row{
        margin-bottom: 16px;
    }
</style>
