2018.11.08  vue �ڹ����û�����Ľ���ʽ���
1.���� script��ǩ������vue.js�ļ�
2. ���Ļ����﷨
html ��
<div id="app">
  {{ message }}
</div>
js��
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }��
  methods��{�Զ��巽����}
})

3.��������
���� v-if   ѭ�� v-for  ��� v-on:click   ��д@click
һ���Բ�ֵ��Ҳ����˵ֵֻ����Ⱦ1�κ������ı�����ֵ����ͬ������Ⱦ�ϣ�v-once
��Ⱦhtml���� v-html
��ȾԪ������ <div v-bind:id="dynamicId"></div>

4.vue����������
beforeCreate������vueʵ��ǰ
created:����vueʵ����  �����ڴ˴���ȡ�����ǹ̶������� ����ӷ�������ȡ���ݣ�����������������
beforeMount:���ص�domǰ
mounted�����ص�dom��
beforeUpdate�����ݱ仯����ǰ
updated�����ݱ仯���º�
beforeDestroy��vueʵ��3����ǰ
destroyed��ʵ�����ٺ�

�� vue���̨���ݽ������axios
�����﷨ axios.post(����php��ַ�ļ��������ݲ�����).then(function(res){��������Ϊһ����������data�Ǵ��ݵ��������� �����������ݴ����header������Ϣ})
��̨���䷽ʽΪ�ļ������� ����json_decodeת�� json_decode(file_get_contents('php://input'),1);

�ĵã�vue���ã�  �����ڵ�  û��Ϥ֮ǰ���úδ�̸��