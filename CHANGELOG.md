# Change Log

## [3.1.0] 2024-02-22

- Update dependencies & devDependencies
- Add support for two-way data binding to `MaterialInput`

## [3.0.0] 2022-06-14

- Update core components name from Vmd to Material.

## [2.0.0] 2022-04-18

### Bug fixing

### Major style changes

- `VmdProgress`'s default `color` value changed to “success” and `percentage` prop type changed from String to Number and set to required.
- `VmdRadio`'s `id`, and `name` props set to required and `checked` prop type changed to Boolean.
- `VmdSocialButton`'s `icon`, `iconOnly`, and `socialBtn` props set to required. `iconOnly` prop type also changed from String to Boolean.
- `VmdSwitch`'s `name`, `id` props set to required. `checked` prop data type changed from String to Boolean. And removed `inputClass` prop and instead any class added to the component will directly be added to input tag.
- `VmdTextArea`'s `id` set to required.
- Added `SalesTableCard` component with the following props and keys:
  - `title` of type String
  - `rows` of type Array and is required.
    - `sales`: of type Number, and String.
    - `value`: of type String
    - `percentage`: of type Number, and String
    - `country`: of type Array
- Added `ChartHolderCard` component with default slot for `chart` component and the : `title`, `subtitle`, `update`, and `color` props of type String.

- Added `BarChart` component with the following props and keys:
  - `id` of type String.
  - `height` of type Number, and String.
  - `chart` of type Object with required value and the following keys:
    - `labels` of type Array.
    - `datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Renamed and refactored `MiniCards` to `MiniStatisticsCard` component and added the following props:
  - Required `title` prop of type Object with the following keys:
    - `text` of type String.
    - `value` of type Number, and String.
  - `detail` of type String.
  - Required `icon` prop type of Object with the following keys:
    - `name`, `color`, and `background` of type String.
- Renamed and refactored `OverviewCard` component to `DefaultStatisticsCard` component with the following props:
  - `title`, `count`, and `menu` of type String.
  - `percentage` of type Object with the following keys:
    - `color`, `value`, and `label` of type String
  - `dropdown` of type Array with the following keys:
    - `label` and `route` of type String.
- Added `PieChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` prop type of Object with the following keys:
    - `labels` of type Array.
    - `datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Added `DefaultLineChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` prop type of Object with the following keys:
    - `labels` of type Array.
    - `datasets` of type Array with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Added `HorizontalBarChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` prop type of Object with the following keys:
    - `labels` of type Array.
    - `datasets` of type Array with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Added `OrdersListCard` component with the following props:
  - `title` of type String.
  - `headers` of type Array.
  - `lists` of type Array with the following keys:
    - `values` of type Array.
    - `title`, `order`, `info`, `image`, and `icon` of type String.
- Added `ProfileInfoCard` component with the following props:
  - `title`, and `description` of type String
  - `Info` of type Object with the following keys:
    - `fullName`, `mobile`, `email`, and `location` of type String.
  - `social` of type Array with the following acceptable keys:
    - `link`, and `icon` of type String.
  - `action` of type Object with the following keys:
    - `route`, and `tooltip` of type String.
- Added `DefaultProjectCard` component with the following props:
  - `image`, `label`, `title`, and `description` of type String.
  - `action` of type Object with the following keys:
    - `route`, `color`, and `label` of type String.
  - `authors` of type array with the following acceptable keys:
    - `image`, and `name` of type String.
- Added `ComplexProjectCard` component with the following props:
  - `image`, `title`, `description`, and `dateTime` of type String.
  - `members` of type Array.
  - `dropdown` of type Array with the following possible keys:
    - `label` and `route` of type String.
- Refactored `DefaultInfoCard` component with the following props:
  - Required `icon` of type String and Object with the following keys:
    - `component`, and `background` of type String.
  - `title`, and `description` of type String.
  - `value` of type String and Number.
- Added `TimelineList` component with `default slot` and the following props:
  - `title`, and `description` of type String.
  - `darkMode` of type Boolean.
- Added `TimelineItem` component with the following props:

  - `color`, `icon`, `title`, `dateTime`, and `description` of type String.
  - `icon` of type object with the following keys:
    - `component` and `class` of type String.

- Refactored `AnimatedStatisticsCard` component with the following props:
  - `color`, and `title` of type String.
  - `count` of type Number and String.
  - `percentage` of type Object with the following keys:
    - `color`, and `label` of type String.
  - `action` of type Object with the following keys:
    - `route`, and `label` of type String.
- Refactored `MiniStatisticsCard` component with the following props:
  - `directionReverse` of type Boolean.
  - `title` of type String and Object with the following keys:
    - `text`, and `color` of type String.
  - Required `value` prop of type String, Number, and Object with the following keys:
    - `text` of type String and Number.
    - `color` of type String.
  - `percentage` of type String and Object with the following keys:
    - `value`, and `color` of type String.
  - `icon` of type String and Object with the following keys:
    - `component`, and `background` of type String.
  - `classContent` of type String.
- Added `AnnouncementCard` component with the following props:
  - `title`, and `description` of type String.
  - `by` of type Object with the following keys:
    - `image`,`name`, and `date` of type String.
  - `badge` of type Object with the following keys:
    - `color`, and `label` of type String.
  - `value` of type Object with the following keys:
    - `currency`, `amount`, and `method` of type String.
  - `action` of type Object with the following keys:
    - `route`, and `label` of type String.
- Refactored `TodoItem` to support dynamic dropdown items with the following props:
  - `title`, `checkboxId`, `dropdownTableId`, `date`, `projectId`, and `company` of type String.
  - `checked` of type Boolean.
  - `action` of type Array with the following possible keys:
    - `label`, and `route` of type String.
- Refactored `PricingCard` component with the following props:
  - `color` of type String.
  - Required `badge` of type Object with the following keys:
    - `color`, `label` of type String.
  - Required `price` of type Object with the following keys:
    - `currency`, `value`, and `charge` of type String.
  - Required `specifications` of type Array with the following possible keys:
    - `label` of type String.
    - `includes` of type Boolean.
  - `action` of type Object with the following keys:
    - `route`, `label`, and `color` of type String.
  - `darkMode` of type Boolean.
- Refactored `InfoCard` component with the following props:
  - `title`, and `description` of type String.
  - `badge` of type Object with the following keys:
    - `text`, and `color` of type String.
- Added the following new props to `ControllerCard` component:
  - `id` of type String.
  - `image` of type Object with the following keys:
    - `url`, `alt`, and `label` of type String.
  - removed `text` prop.
- Refactored `ProgressLineChart` component with the following props:
  - `id`, `height`, `icon`, and `title` of type String.
  - `count`, and `progress` of type Number.
  - Required `chart` of type Object with the following keys:
    - `labels`, and `data` of type Array.
- Added `DefaultItem` component with the following props:
  - `title`, and `description` of type String.
  - `icon` of type Object with the following keys:
    - `component`, and `color` of type String.
- Refactored `LineChart` component with the following props:
  - `id`, `height`, and `title` of type String.
  - `value` of type Object with the following keys:
    - `amount` of type String.
    - `percentage` of type object with the following keys:
      - `value` of type Number and String.
      - `color` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - `datasets` of type Object with following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `MiniInfoCard` component with the following props:
  - `icon`, `color`, `title`, and `description` of type String.
- Following minor changes were made to `MusicPlayer` component.
  - removed `title`, and `description` props.
  - Added `color` prop of type String
  - Added `song` prop type of Object with the following keys:
    - `title`, and `singer` of type String.
- Refactored `Calendar` component with the following props:
  - `id`, `title`, `day`, `year`, `initialView`, and `initialDate` of type String.
  - `events` of type Array.
  - `selectable` of type Boolean with the default value of `true`.
  - `editable` of type Boolean with the default value of `true`.
- Added `CategoriesList` component with the following props:
  - `title` of type String.
  - `items` of type Array with the following possible keys:
    - `title`, and `description` of type String.
    - `icon` of type Object with the following keys:
      - `component`, and `background` of type String.
- Added the following props to `GradientLineChart` component.
  - Required `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - `datasets` of type Array with the following possible keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored the `BarChart` with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `BarChartHorizontal` with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `MixedChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Array with the following possible keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `BubbleChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Array with the following possible keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `DoughnutChart`component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `RadarChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Array with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `PolarChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Object with the following keys:
      - `label` of type String.
      - `data` of type Array.
- Refactored `EventsCard` component with the following props:
  - `title` of type String.
  - `events` of type Array with the following possible keys:
    - `icon`, `color`, `event`, and `date` of type String.
- Added `MiniLineChart` component with the following props:
  - `id`, and `height` of type String.
  - Required `chart` of type Object with the following keys:
    - `labels` of type Array.
    - Required`datasets` of type Array with the following possible keys:
      - `label` of type String.
      - `data` of type Array.
- MasterCard `props` refactored to a single `card` prop `Object` with the following keys:
  - `number` accepts a `String` with the default value of `7852 4594 1122 4562`.
  - `holderText` accepts a `String` with the default value of `Card Holder`.
  - `holderName` accepts a `String` with the default value of `Jack Peterson`.
  - `expiryText` accepts a `String` with the default value of `Expirs`.
  - `expiryDate` accepts a `String` with the default value of `11/22`.
  - `background` accepts a `String` with the default value of `dark`.
- `VmdAlert` 's `img` prop renamed to `image` and set to `required`.
- `VmdButton`'s `color` prop default value set to `success`.
- `VmdCheckbox`'s `checked` prop type changed from `String` to `Boolean`.
- The following minor changes were made to `VmdSnackbar`.
  - `title` prop set to required.
  - Deleted `iconColor` and `iconName` props.
  - Added `icon` prop type of object with `component`, and `color` keys.
- Renamed `ChartBars` component to `BarChart` component.
- Extracted `PieChart` component from `ChannelsChartCard` component to its own component.
- Renamed `EarningsCard` component to `AnimatedStatisticsCard` component.
- Renamed `Card` component to `MiniStatisticsCard` component.
- Renamed `FullBodyCard` component to `InfoCard` component.
- Renamed `TasksCard` component to `ProgressLineChart` component.
- Following minor changes were made to `StepsCard` component.
  - `steps` renamed to `count`.
  - Added `badge` prop type of Object with the following keys:
    - `label`, and `color` of type String.
- Renamed `LineChartGradient` to `GradientLineChart` component.
- All `BookingCard` props are set to required.

### Deleted components

```
SalesTableCard.vue
ChartHolderCard.vue
ReportsBarChart.vue
ReportsLineChart.vue
PieChart.vue
DefaultLineChart.vue
HorizontalBarChart.vue
OrdersListCard.vue
ProfileInfoCard.vue
DefaultProjectCard.vue
ComplexProjectCard.vue
TimelineList.vue
TimelineItem.vue
AnnouncementCard.vue
DefaultItem.vue
CategoriesList.vue
MiniLineChart.vue
```

### Added components

```
SalesTableCard.vue
ChartHolderCard.vue
ReportsBarChart.vue
ReportsLineChart.vue
PieChart.vue
DefaultLineChart.vue
HorizontalBarChart.vue
OrdersListCard.vue
ProfileInfoCard.vue
DefaultProjectCard.vue
ComplexProjectCard.vue
TimelineList.vue
TimelineItem.vue
AnnouncementCard.vue
DefaultItem.vue
CategoriesList.vue
MiniLineChart.vue
```

### Deleted dependencies

```
@fullcalendar/vue
@fullcalendar/vue3
countup.js
```

### Added dependencies

```
@fortawesome
```

### Updated dependencies

### Warning

## [1.0.0] 2022-02-28

### Original Release
