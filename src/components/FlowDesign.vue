<template>
  <div class="flow-design">
    <img :src="background" />
    <v-data-table :headers="headers" :items="desserts" class="elevation-1">
      <template v-slot:items="props">
        <td>{{ props.item.name }}</td>
        <td class="text-xs-right">{{ props.item.code }}</td>
        <td class="text-xs-right">{{ props.item.description }}</td>
      </template>
    </v-data-table>
  </div>
</template>
<script>
import bg from "../assets/flow_design.png";
export default {
  name: "FlowDesign",
  data: () => {
    return {
      background: bg,
      headers: [
          {
            text: '字段名称',
            align: 'left',
            sortable: false,
            value: 'name'
          },
          { text: '字段编码', value: 'code' },
          { text: '字段描述', value: 'description' }
        ],
        desserts: [
          {
            name: '账户金额',
            code: 'accountBalance',
            description: '用户账户上的余额',
          },
          {
            name: '用户信息',
            code: 'userInfo',
            description: '用户的各种信息',
          },
          {
            name: '验证审核',
            code: 'authentication',
            description: '验证审核信息',
          },
          {
            name: '已买基金',
            code: 'listCompany',
            description: '已经购买的基金',
          },
          {
            name: '已买股票',
            code: 'listStock',
            description: '已经购买的股票',
          }
        ]
    };
  },
};
</script>
