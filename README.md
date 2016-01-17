# mytableplus
一个table表插件

使用方法(详见js中的参数说明)：
function getCrossOverList(){
    var col=[
        {title:"管道名称",name:"lineName",width:"10%",align:"center"},
        {title:"管段名称",name:"segmentName",width:"10%",align:"center"},
        {title:"穿跨越编号",name:"crossingNumber",width:"5%",align:"center"},
        {title:"穿跨越类型",name:"crossingType",width:"5%",align:"center"},
        {title:"穿跨越名称",name:"crossingName",width:"5%",align:"center"},
        {title:"穿跨越对象",name:"crossingTarget",width:"5%",align:"center"},
        {title:"穿跨越方式",name:"crossingMethod",width:"5%",align:"center"},
        {title:"起点绝对距离",name:"fromMileage",width:"10%",align:"center"},
        {title:"穿跨越长度(m)",name:"crossingLength",width:"10%",align:"center"},
        {title:"详情 删除",name:"",width:"5%",align:"center",format:dataDeatil}
        /*{title:"删除",name:"",width:"5%",align:"center",format:dataDel}*/
    ];
    $("#pipeCrossOver").initTable({
        url: p_path + "/pipe/PipeCrossDataM/queryPipeCrossList.json",
        columnData: col,
        doubleRowMode:true,
        isrowClick:true,
        maxHeightMode:true,
        rowClickMethod:pipeCrossOverRowClick,
        selectDataNow:true
    });
}
