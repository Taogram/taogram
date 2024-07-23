<!--
 * @Description: 
 * @Version: 1.0.0
 * @Author: lax
 * @Date: 2023-05-06 18:35:54
 * @LastEditors: lax
 * @LastEditTime: 2024-07-23 23:10:03
-->
# Taogram
Tao即道，这是一个关于道的项目，该项目致力于将中国三式占卜等术进行程序化。

---

## 快速导航
### 术
* [奇门遁甲](https://github.com/Taogram/taobi)
* [奇门图解](https://github.com/Taogram/tao_tools)
* 八字(TODO)
* 梅花易数(TODO)

### 天干五行
* [干支历](https://github.com/Taogram/calendar)
* [易名](https://github.com/Taogram/tao_name)
* [阴阳五行](https://github.com/Taogram/taichi)
* [万年历改](https://github.com/Taogram/DBWnl)
### 天文相关
* [章动](https://github.com/Taogram/nutation.js)
* [儒略日](https://github.com/Taogram/julian.js)
* [二十四节气](https://github.com/Taogram/solar_terms.js)

## 开始

### 历法相关
* 公历转干支历
凡式术，无不离干支之历。无论后续如何起式，第一步都需要先计算出生辰八字。
    1. 如果需要进行干支历转化的可以使用[[干支历]Calender](https://github.com/Taogram/calendar.git)。
    2. 干支历由于六十甲子一循环，就有了循环的起点说法，如果你想要自定义或确认程序的干支历起始问题，你可以参考[[干支历]Calender](https://github.com/Taogram/calendar.git)。（该内容待更新）
    3. 干支历古人通过观测北斗七星的周期而确认，也就是根据地球视角的太阳循环一周的周期来判断年月。而每年的起始则又有不同取法，如建寅、建丑等，并且者往往也不同于现今公历的时间。因此什么时候为月建就会影响干支历的取用，详细可见XXX。（同样待更新）
    4. 转化过程中因为需要进行天体计算因此公历中的UTC需要转化为对应的力学时TD，查看转化算法和相关内容，你可以参考[[儒略日]](https://github.com/Taogram/julian.js)。
* 二十四节气的计算
    1. 二十四节气对应的是地球公转的角度，每15°一节气。因此每一个节气的计算就涉及到天文计算，关于二十四节气的包请参考[[二十四节气]SolarTerms.js](https://github.com/Taogram/solar_terms.js.git)。
    2. 天文计算中，算法采用的是VSOP87D，天体算法的数据量较为庞大，简化数据有利于快速计算，关于全量数据和简化数据的对比可以参考[[二十四节气]SolarTerms.js](https://github.com/Taogram/solar_terms.js.git)。
    3. 天文计算中，计算得到的经度还需要经过章动修正和广行差修正，其中章动算法涉及到IAU1980和IAU2000B，具体结果对比可以参考[[二十四节气]SolarTerms.js](https://github.com/Taogram/solar_terms.js.git)。
    4. 目前整体的二十四节气差值和官方公布的差别在1~2分钟，该精度完全适用于易学相关的节气计算。

### 易之基
* 阴阳五行
    1.易学的基础无不离阴阳与五行，详情可参考[[阴阳五行]](https://github.com/Taogram/taichi)。
* 天干地支
    1.天干地支的旺相休囚死，合冲刑害等关系，可以参考[[干支历]Calender](https://github.com/Taogram/calendar.git)。

### 奇门遁甲
* 奇门摆盘
奇门以年月日时家分列，常有者为时家奇门。
    1. 如果需要进行奇门摆盘则可以使用[[奇门遁甲]Taobi](https://github.com/Taogram/taobi.git)，如果你对奇门的用神分布尚不熟练还可以使用本项目原创的[[奇门图解]TaoTools](https://github.com/Taogram/tao_tools)进行解盘。
    2. 由于干支历年月取法公转、日时则取法自转。因此存在日不尽月的情况，这也就有用局计算的拆补法和置润法等一说。本项目仅采用拆补法一种，究其理为其法合乎天理。古人受限天文计算精度问题才有了置润一法，而现今天文计算则完全可以将周期精确到秒的平分为二十个节气或者说十二个月，这样的精度足以奇门用局所用。若需要详细明确本项目的用局计算则可以参考[[二十四节气]SolarTerms.js](https://github.com/Taogram/solar_terms.js.git)。
    3. 除此以外，奇门还有分盘法和转盘法，本项目当前仅有转盘一法，尚待更新。
    4. 奇门摆盘又涉及如何处理用局定局问题，具体又分为茅山法、置润法、拆补法，其中本项目根据用局源于二十四节气的核心逻辑又原创的均分法，具体可以参考[[奇门遁甲]Taobi](https://github.com/Taogram/taobi.git)。
    5. 奇门摆盘结果以九宫显示，若需要定制奇门个宫的用神显示位置可以参考XXX（TODO）。
    6. 暗干
    7. 转盘寄宫
    8. ...

## [易之理，中英译法] chinese->english
### 阴阳
* 《道德经》：道可道，非常道，名可名，非常名
* 《道德经》：道生一，一生二，二生三，三生万物
* 《道德经》：有物混成，先天地生。寂兮寥兮，独立而不改，周行而不殆，可以为天地母。吾不知其名，强字曰为道。

道之名也，不可谓之全，强字谓道亦可谓太极，太极生二，是为阴阳。阴阳者，不过盛衰之分，有无之辩

* 《道德经》：反者道之动。弱者道之用。天下万物生于有，有生于无。

固先无而后有，有生于无，有因无而有。
无者，为始，为空，固取零而示之。
有者，为起，为存，固取一而示之。

因此0为无亦为阴，1为有亦为阳，当是合乎其理。

#### logos
逻各斯（LOGOS），赫拉克利特提出的类逻辑规律概念，为西方最早的抽象用词，固取其以表阴阳。

### 五行


## Installation

## Q&A

## 联系
### WX: taogram
### EMAIL: 1546356935@qq.com