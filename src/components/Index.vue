<template>
  <div class="layout">
    <Menu mode="horizontal" theme="dark" active-name="1">
      <div class="layout-logo"></div>
      <div class="layout-nav">
        <Submenu name="3">
          <template slot="title">
            <Icon type="ios-person"></Icon>
            超级管理员
        </template>
          <MenuGroup title="设置">
            <MenuItem name="3-1">修改信息</MenuItem>
            <MenuItem name="3-2">修改密码</MenuItem>
            <MenuItem name="3-3">其他设置</MenuItem>
          </MenuGroup>
          <MenuGroup title="管理">
            <MenuItem name="3-4">退出</MenuItem>
          </MenuGroup>
        </Submenu>
      </div>
    </Menu>
    <div class="layout-content">
      <Row>
        <Col span="5">
        <Menu active-name="1-2" width="auto" :open-names="['1']">
          <Submenu name="1">
            <template slot="title">
              <Icon type="ios-navigate"></Icon>
              Item 1


            </template>
            <MenuItem name="1-1">Option 1</MenuItem>
            <MenuItem name="1-2">Option 2</MenuItem>
            <MenuItem name="1-3">Option 3</MenuItem>
          </Submenu>
          <Submenu name="2">
            <template slot="title">
              <Icon type="ios-keypad"></Icon>
              Item 2


            </template>
            <MenuItem name="2-1">Option 1</MenuItem>
            <MenuItem name="2-2">Option 2</MenuItem>
          </Submenu>
          <Submenu name="3">
            <template slot="title">
              <Icon type="ios-analytics"></Icon>
              Item 3


            </template>
            <MenuItem name="3-1">Option 1</MenuItem>
            <MenuItem name="3-2">Option 2</MenuItem>
          </Submenu>
        </Menu>
        </Col>
        <Col span="19">
        <div class="layout-content-main">Content</div>
        </Col>
      </Row>
    </div>
    <div class="layout-copy">
      2011-2016 &copy; TalkingData


    </div>
  </div>
</template>

<script>
  export default {
    name: 'index',
    data() {
      return {
        msg: ''
      }
    },
    methods: {
      handleSelect: function () {

      }
    }
  }
</script>

<style>

  .layout {
    border: 1px solid #d7dde4;
    background: #f5f7f9;
  }

  .layout-logo {
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 15px;
    left: 20px;
  }

  .layout-nav {
    float: right;
  }

  .layout-assistant {
    width: 300px;
    margin: 0 auto;
    height: inherit;
  }

  .layout-breadcrumb {
    padding: 10px 15px 0;
  }

  .layout-content {
    min-height: 200px;
    margin: 15px;
    overflow: hidden;
    background: #fff;
    border-radius: 4px;
  }

  .layout-content-main {
    padding: 10px;
  }

  .layout-copy {
    text-align: center;
    padding: 10px 0 20px;
    color: #9ea7b4;
  }

</style>
