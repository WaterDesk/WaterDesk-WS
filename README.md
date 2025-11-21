# WaterDesk

WaterDesk 慧水供水模型软件

近几年，随着智慧水务建设节奏逐步加快，供水管网模型成为行业聚焦热点，利用模型对管网运行数据进行挖掘也变为现实。如何降低建模的门槛，使模型成为供水企业重要的技术工具，从而加快企业实现智慧水务的步伐是我们一直追求的目标。为此，我们于 2019 年开发了一款功能完整的供水模型软件---WaterDesk，致力于帮助企业能够快速且高效建立供水管网模型。

WaterDesk 软件功能完善、操作便捷、界面美观，适用于不同信息化阶段的供水企业对各种复杂工况环境的模拟需求。软件支持主流的数据格式，如 INP，SHP，DXF 和 Excel 等；具有专业的运营分析功能，如水厂停运缺水分析、管网分区设计、供水范围审查和管网运行诊断等；并通过便捷的图例、标注功能以及丰富的表格、曲线展示提高了软件的易用性。

诚挚欢迎各位同仁光临公司网站[http://www.info-water.com](http://www.info-water.com)下载使用，也热忱地希望大家给我们的软件提出建议，让我们共同为智慧水务建设尽微薄之力。

上海慧水科技有限公司

![WaterDesk](./images/WaterDesk_01.png)

## System Requirements

- System requirements for WaterDesk Educational

  |                      |                                                              |
  | -------------------- | ------------------------------------------------------------ |
  | **Operating System** | 64-bit Microsoft® Windows® 11 and Windows 10                 |
  | **Processor**        | **Basic**: 2.5-2.9 GHz processor with 8 logical cores (base) |
  |                      | **Recommended**: 3+ GHz processor (base), 4+ GHz (turbo)     |
  | **Memory**           | **Basic**: 16 GB                                             |
  |                      | **Recommended**: 64 GB                                       |
  | Display Resolution   | 1920 x 1080 with True Color                                  |
  | Disk Space           | 500G (suggested SSD)                                         |
  | .NET Framework       | .NET Framework version 4.8                                   |
  | VC Runtime           | Visual C++ Redistributable for Visual Studio 2015-2022       |

## Release Notes

### version 6.0.0

- support undo/redo
- support tianditu map
- EPANET bug fixes
- [reset valve setting when valve status changes to be a fixed status (OPEN/CLOSED) by controls](https://github.com/OpenWaterAnalytics/epanet-dev/pull/66)
- some other performance/UI improvement and bug fixes

### version 5.0.0

- upgrade network topologies by differencing GIS changes
- generate demand patterns by clustering algorithms to identify water user groups
- connect with WaterDesk-Live system, upload/download models to/from online system with latest SCADA time data
- model file encryption
- AI assistant "XIAOHUI"
- find shortest path by given two objects
- some other UI improvement and bug fixes

### version 4.0.0

- object properties
  - Pattern: add more pattern types: reservoir level, inflow of tank, outflow of tank, quality
  - all Link objects: add control item count, display it in property palette and table
- new features and improvement
  - energy report
  - display selection sets as tree structure by using path separator '/', e.g. level-1/item
  - highlighting rows in tables when selecting object in the map
  - add a simulation option: ignore invalid controls which referenced objects are invalid during simulation
  - view: highlight Link objects with controls
  - view: highlight boundary conditional SCADA points
  - refactor Time Pattern Editor window as modeless
  - refactor Background layers manager, allow import as model objects in batch
  - show profile graph for link objects
  - analyze the relationship between Flow and Pressure SCADA group
  - some other UI improvement and bug fixes

### version 3.1.0

- some bug fixes

### version 3.0.0

- object properties
  - all objects: add note6 ~ note10 fields
  - pump: add Rated Flow, Rated Head, Frequency Mode(Fixed/Variable), Max Frequency and Min Frequency
  - Quality SCADA: add Chlorine and Turbidity types
  - Pattern: add two virtual patterns, total energy and total efficiency
- new features and improvements:
  - merge model files by importing a .wdm file
  - add model precision analysis for the China Urban Water Association group standard (T/CUWA20059-2022)
  - add analysis settings, such as minimum flow and minimum velocity
  - selection mode in Status Bar: controls the selection mode with overlapping objects
  - navigation mode in Status Bar: controls the navigation mode by moving or zooming
  - allow users to clear, load, unload simulation results
  - graph window: add level and head properties of Level SCADA, customize the max and min values of the Y-axis
  - Control Editor window: display control items in a table
  - import SCADA time data: specify a time range and discard the seconds component
  - performance improvement, such as network simplification, select a large number of objects in table and highlight them in the map, delete a large number of objects, play mode, etc.
  - some UI improvements and bug fixes
- EPANET bug fixes
  - [fix - OptionParser::parseQualOption doesn't consider the cases for "Quality Trace" mode: the trace node has not been specified; the specified trace node doesn't exist](https://github.com/OpenWaterAnalytics/epanet-dev/pull/61)
  - [fix - the last volume segment should be initialized as the first volume segment during initializing a tank's mixing model](https://github.com/OpenWaterAnalytics/epanet-dev/pull/62)
- Online Support (need registration): there are some advanced features which are used to connect WaterDesk Online System
  - import billings
  - allocate billings to customers as demands
  - allocate demands by region
  - scheduling optimization for a plant
  - deploy the model to Cloud as an Online System
  - upgrade the model to an existing Online System

### version 2.3.0

- polygonal selection
- add Plant, Pump Station objects
- support enable/disable status for model objects
- add Zone object
- Zone analysis for completeness, bind Flow SCADA to Zone semi-automatically
- add virtual pattern
- add virtual SCADA, support Model value expressions: `PRESSURE()`, `FLOW()`, `QUALITY()`
- support search in Time Pattern Editor window
- fix some EPANET bugs about quality simulation
- some UI improvements
- some bug fixes

### version 2.2.0

- quick search bar
- open recent folders
- save and edit project notes
- customize the content for objects' labels
- find the neighbor junctions of which the difference of elevation or head exceeds the threshold
- pressure influence coverage analysis
- delete unused result files automatically
- calculate the reliability for Pressure and Flow SCADAs
- analysis the flow and demand data of DMA
- some UI improvements
- some bug fixes

### version 2.1.0

- improve the graphics performance, especially displaying the labels of model objects
- legend settings for Pressure, Flow and Quality SCADA objects
- add Text Label with/without referencing model objects
- style settings for Object Labels and Text Label
- allow multiple graph chart windows to be pinned
- some bug fixes

### version 2.0.0

- update pattern values from SCADA by JS expressions
- measure distance in map
- add legend setting for Customers
- add flow/pipe direction arrow display setting
- add FCI (Flow Calibration Index) analysis
- optimize trace up/down
- optimize demand allocation
- optimize selection set operations
- display head for Pressure SCADA in result graph
- Flow SCADA can be converted to Transfer Flowmeter
- SCADA points' Error chart / Objects' difference in result graph
- support more data file format for SCADA time data (.csv)
- support database source for SCADA time data (Access, Sqlite, SQL Server)
- support search in SCADA Browser window
- export to Infoworks' calibration data files
- support data transform when import SCADA time data
- Some bug fixes and performance improvement

### version 1.5.0

- Demand allocation by referencing to Customers
- Fix EPANET bugs: some Pump Curve's bugs during simulation calculation
- Add PCI (Pressure Calibration Index) analysis
- Add more SCADA objects: Frequency (for Pump), Energy (for Pump), Switch (for Pump or Valve), and Level (for Reservoir or Tank)
- Support Baidu Earth for web map
- Some bug fixes

### version 1.4.0

- Add recent file list
- Fix EPANET bug: apply pressure control during ggasolver
- Pump curve fitting
- Some bug fixes

### version 1.3.0

- Add Baidu Map
- Fix EPANET bug: reset speed to 0.0 if change pump status to LINK_CLOSED
- Some bug fixes and performance improvement
