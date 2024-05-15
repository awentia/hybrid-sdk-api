# Awentia Hybrid Cloud API Documentation

A comprehensive guide to using the Hybrid Cloud API to configure Awentia's smart camera.

## Navigation
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage Examples](#usage-examples)
- [Function Descriptions](#function-descriptions)
- [Output Database Format](#output-database-format)

## Installation

To install Awentia's Hybrid Cloud API, follow these steps:

```
git clone https://example.com/hybridcloudapi.git
cd hybridcloudapi && npm install
```

## Configuration

Configure the API by setting the capture frequency and detection prompts as shown below:

```
api.setDevice('/dev/video0');
api.setFrequency('10 Hz');
api.setPrompt('count the clusters in the photo');
api.setOutputFormat('/tmp/outputFormat.xml');
```

## Output Database Format

The format of the output database record is as follows in an XML file:

```xml
<record>
  <image_timestamp>timestamp of the image</image_timestamp>
  <prompt_result>textual result of the prompt</prompt_result>
  <prompt_result_formatted_output>XML file of the textual result</prompt_result_formatted_output>
  <category_id>object category</category_id>
  <bbox>
    <xmin>value</xmin>
    <ymin>value</ymin>
    <width>value</width>
    <height>value</height>
  </bbox>
  <segmentation>array of polygons</segmentation>
  <area>object area</area>
</record>
```

## Usage Examples

Example of using the API to start a detection session:

```
api.startDetection();
```

## Function Descriptions

**startDetection()**: Starts the detection session.

**setFrequency(frequency)**: Sets the camera's capture frequency.

**setPrompt(prompt)**: Defines the detection prompt for the session.

## Footer

© 2024 Awentia Hybrid Cloud API. All rights reserved.
```
