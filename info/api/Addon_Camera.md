---
layout: default-layout
needAutoGenerateSidebar: true
title: Dynamic Web TWAIN API Reference - Camera Addon APIs
keywords: Dynamic Web TWAIN, Documentation, API Reference, Camera Addon APIs
breadcrumbText: Camera Addon
description: Dynamic Web TWAIN SDK Documentation API Reference Camera Addon APIs Page
permalink: /info/api/Addon_Camera.html
---

# `{WebTwainObject}.Addon.Camera`

> {WebTwainObject} denotes the `WebTwain` instance.

Dynamic Web TWAIN comes with a Camera add-on for you to capture images or documents using MediaDevices cameras, auto crop and adjust perspective. 

To include the Camera add-on, simply add a reference to the corresponding camera JS file:

``` html
<script src="Resources/addon/dynamsoft.webtwain.addon.camera.js"></script>
```
Check out [MediaDevices Cameras]({{site.indepth}}features/input.html#use-mediadevices-cameras) to learn more on how to use the camera add-on.

**Methods**

|                                     |
| :---------------------------------- | :---------------------------------- | ------------------------------------------------- | --------------------------------- |
| [`getSourceList()`](#getsourcelist) | [`selectSource()`](#selectsource)   | [`getCurrentSource()`](#getcurrentsource)         | [`closeSource()`](#closesource)   |
| [`getResolution()`](#getresolution) | [`setResolution()`](#setresolution) | [`getCurrentResolution()`](#getcurrentresolution) | [`play()`](#play)                 |
| [`pause()`](#pause)                 | [`resume()`](#resume)               | [`stop()`](#stop)                                 | [`getStatus()`](#getstatus)       |
| [`capture()`](#capture)             | [`showVideo()`](#showvideo)         | [`closeVideo()`](#closevideo)                     | [`scanDocument()`](#scandocument) |

**Events**

|                                   |
| :-------------------------------- | :-------------------------- | 
| [`video-closed`](#video-closed) | [`video-error`](#video-error) | 

---

## getSourceList

**Syntax**

```typescript
/**
 * Return a list of all available cameras.
 */
getSourceList(): Promise<DeviceInfo[]>;

interface DeviceInfo{
    deviceId: string;
    label: string;
}
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
</tr>

</table>
</div>

**Example**

```javascript
DWObject.Addon.Camera.getSourceList();
```

---

## selectSource

**Syntax**

```typescript
/**
 * Select a camera to use.
 * @param deviceId Specify the camera with its deviceId.
 */
selectSource(deviceId: string): Promise<DeviceInfo>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
</tr>

</table>
</div> 

---

## getCurrentSource

**Syntax**

```typescript
/**
 * Return the info about the current camera.
 */
getCurrentSource():DeviceInfo;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
</tr>

</table>
</div>

---

## closeSource

**Syntax**

```typescript
/**
 * Close the current camera.
 */
closeSource(): Promise<DeviceInfo>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## getResolution

**Syntax**

```typescript
/**
 * Return the resolutions supported by the current camera.
 */
getResolution(): Promise<Resolution[]>

interface Resolution{
    width: number;
    height: number;
}
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## setResolution

**Syntax**

```typescript
/**
 * Set the resolution for the current camera.
 * @param resolution Specify the resolution.
 */
setResolution(resolution: Resolution): Promise<Resolution>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## getCurrentResolution

**Syntax**

```typescript
/**
 * Return the resolution of the current camera.
 */
getCurrentResolution(): Promise<Resolution>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

**Usage notes**

If the camera is playing, the actual resolution is returned. If the camera is not playing, the last set resolution or null is returned.

---

## play

**Syntax**

```typescript
/**
 * Start streaming video from the current camera.
 * @param element Specify an HTML element to put the video stream in.
 * @param resolution Specify the initial resolution.
 * @param fill Whether to fill the viewer space with the video stream and leave no margin. The default value is `false`.
 */
play(element?: HTMLElement,
    resolution?: Resolution,
    fill?: boolean
): Promise<Resolution>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

**Usage notes**

If no camera is chosen, the default camera is used.

If the method is called without arguments or `null` is passed to `element` , the video will show in the main viewer.

---

## pause

**Syntax**

```typescript
/**
 * Pause the video stream.
 */
pause(): void;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>
---

## resume

**Syntax**

```typescript
/**
 * Resume the video stream.
 */
resume(): void;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## stop

**Syntax**

```typescript
/**
 * Stop the video stream.
 */
stop(): void;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## getStatus

**Syntax**

```typescript
/**
 * Return the status of the current camera.
 */
getStatus(): string;
```

**Usage notes**

The status string is either empty or one of the following: "playing", "paused", "stopped". An empty string means no camera is open.

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>
---

## capture

**Syntax**

```typescript
/**
 * Capture a frame from the video stream.
 */
capture(): Promise<Blob>;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

---

## closeVideo

**Syntax**

```typescript
/**
 * Close the camera and hide the video streaming UI.
 */
closeVideo(): void;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+ </td>
<td align="center">v16.1+</td>
<td align="center">v16.1+</td>
</tr>

</table>
</div>

## video-closed

**Syntax**

``` typescript
/**
 * This event is triggered when the video is closed.
 */
on("video-closed", callback: () => void): boolean;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.2+ </td>
<td align="center">v16.2+</td>
<td align="center">v16.2+ </td>
<td align="center">v16.2+</td>
<td align="center">v16.2+</td>
</tr>

</table>
</div>

---

## video-error

**Syntax**

``` typescript
/**
 * This event is triggered when the video playing operation. throws out an error.
 * @argument errorCode The error code.
 * @argument errorString The error string.
 */
on("video-error", callback: (errorCode, errorString) => void): boolean;
```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported  </td>
<td align="center">v16.2+ </td>
<td align="center">v16.2+</td>
<td align="center">v16.2+ </td>
<td align="center">v16.2+</td>
<td align="center">v16.2+</td>
</tr>

</table>
</div>

## scanDocument

**Syntax**

``` typescript
/**
 * Open the camera to capture document(s).
 * @param documentConfiguration Specify the document configuration.
 */
scanDocument(documentConfiguration?: DocumentConfiguration
): Promise<Resolution>;

interface DocumentConfiguration {
  scannerViewerSettings?: ScannerViewerSettings,
  documentEditorSettings?: DocumentEditorSettings
}

interface ScannerViewerSettings {
  element?: HTMLDivElement, //Bind the element or element id. 
                            //After binding, display the video in the specified element, otherwise, display the video in full screen.
  deviceId?: string,  
  maxDocuments?: number,       //The maximum documents can be captured/loaded in to the buffer. 
  enableBorderDetection?: boolean,  // Whether to enable border detection. The default value is true.
  fullScreen?: boolean,   //Whether to display the video in full screen. The default value is false.
  polygonStyle?:{      //The sytle of the auto detect border.       
    stroke: string,    //default: "#fe8e14". Only supports #16 hexadecimal.
    strokeWidth: string,  //default: "2px"
    dash: string          //The allowed value are "solid" and "dashed", the default value is "solid".
    },
  headerStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    color: string,  //The color of the icons. Default : "#ffffff". Only supports #16 hexadecimal.
    selectedColor: string,  //The color of the selected icon. Default : "#fe8e14". Only supports #16 hexadecimal.
  },
  bodyStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    loaderBarSource: string, //The image source of the loader bar: url (e.g. "https://xxx.png") or base64
  },
  footerStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    color: string,  //The color of the icons. Default : "#ffffff". Only supports #16 hexadecimal.
    selectedColor: string,  //The color of the selected icon. Default : "#fe8e14". Only supports #16 hexadecimal.
  },
  scanButtonStyle?:{
    background: string,  //default: "#fe8e14". Only supports #16 hexadecimal.
    color: string,  //Default : "#ffffff". Only supports #16 hexadecimal.
  },      
  resolution?:{
    visibility?: boolean, //Whether to display the resolution icon in the upper left corner. The default value is true.
    valueList?:[ {   
      label: string,    //The resolution value listed in the drop-down list. For example："1920x1080"
      value: Resolution //The resolution you set. For example: { width:1920, height:1080}
    },{……}]
      defaultValue?: Resolution , //Set the default value according to the value set in the valueList.
    },
  autoScan?:{   //Automatically capture when a clear document is detected. Only applicable to video scanning. 
      visibility?: boolean,     //Whether to display the automatic scan icon. The default value is true.
      enableAutoScan?: boolean, //Whether to enable automatic scan. The default value is false.
      },
  autoDetect?:{  //Only applicable to video scanning.                  
      visibility?: boolean,         //Whether to display the automatic border detection icon. The default value is true.
      enableAutoDetect?: boolean,   //Whether to enable automatic border detection. The default value is false.     
      acceptedPolygonConfidence?: number, //The default value is 80. The higher the setting, the more accurate the automatic border detection.
      fpsLimit?: number,  //The maximum number of frames detected per second. The default value is 3.
      },     
  continuousScan?: boolean, //Whether to enable continuous scan. The default value is true.
  switchCamera?:{  //The default camera is the rear camera.
      visibility?: boolean,   //Whether to display the switch camera icon. The default value is true.
      },
  loadLocalFile?:{  
      visibility?: boolean,   //Whether to display the load local file icon. The default value is true.
      },
  funcConfirmExit?: funcConfirmExit, 
    //funcConfirmExit is the callback funtion
    //Return true：End this capture without saving the image data. Return false: Stay on the original viewer
},

interface DocumentEditorSettings {
  visibility: true,
  element?: HTMLDivElement, //Bind the element or element id. 
                            //After binding, display the video in the specified element, otherwise, display the video in full screen.  
  defaultViewerName: string,  //value: "cropViewer", "mainViewer". default: "crop Viewer
  headerStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    color: string,  //The color of the icons. Default : "#ffffff". Only supports #16 hexadecimal.
    selectedColor: string,  //The color of the selected icon. Default : "#fe8e14". Only supports #16 hexadecimal.
    disableColor: string,  //default: "#808080"
  },
  bodyStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    loaderBarSource: string, //The image source of the loader bar: url (e.g. "https://xxx.png") or base64
  },
  footerStyle?:{
    background: string,  //default: "#000000". Only supports #16 hexadecimal.
    color: string,  //The color of the icons. Default : "#ffffff". Only supports #16 hexadecimal.
    selectedColor: string,  //The color of the selected icon. Default : "#fe8e14". Only supports #16 hexadecimal.
  },  
  insert?: {  //Insert an image  
    visibility?: boolean,   //Whether to display the insert icon. The default value is true.
    position?: string,   //Set whether to insert the image "before" or "after" the current image. The default value is "before".
  },
  remove?: { //Remove an image
    visibility?: boolean,   //Whether to display the remove icon. The default value is true.
    funcConfirmRemove: funcConfirmRemove,
  },
  rotateLeft?: { 
    visibility?: boolean,   //Whether to display the rotate left icon. The default value is true.
  },
  filter?: {
    visibility?: boolean,   //Whether to display the filter icon. The default value is true.
    valueList?:[ {  //If not specified, listing all the filters in the order of original, blackAndWhite, grayscale, clean, brightening, saveToner by default. 
                    //Support adjusting the valueList order to arrange the filter order.
      label: string,   //The label of the filter. For example. The filter "Original" can be modified to any word you want to describe
      value: string,   //The filter value. The value must be set according to our specification below.
    //Allowed values: original, blackAndWhite, grayscale, clean, brightening, saveToner	
      option?: {
        level: 1  //The filter level. The allowed values are 1(default value), 2, 3.
                  //The higher the level, the better the quality, but the more time it takes.
        }
    },{……}]
    defaultValue?: string,   //Filter selected by default. By default, the original filter is selected.
    applyToAll?: {
      visibility?: string, //"visible"：hidden". Default："visible"
      enableApplyToAll?: boolean, //Default:false
      label: string, //Default: "Apply to all"
    }
  },
  crop: {
    visibility: boolean,  //Default："visible"
  },
  cropViewer: CropViewer,
  funcConfirmExit: funcConfirmMainViewerExit,
  funcConfirmExitAfterSave: funcConfirmExitAfterSave,
},

interface CropViewer {
  visibility?: boolean,   //Whether to display the crop viewer. The default value is true. 
  polygonStyle?:{    //The polygon style in the crop viewer.       
    stroke: string,       //default : "#fe8e14".  Only supports #16 hexadecimal.
    strokeWidth: string,   //default: "2px"
    dash: string           //The allowed value are "solid" and "dashed", the default value is "solid".
    },
  rotateLeft?:{   
    visibility?: boolean,   //Whether to display the rotate left icon. The default value is true.
    },
  rotateRight?:{   
    visibility?: boolean,   //Whether to display the rotate right icon. The default value is true.
    },
  autoDetectBorder?:{   
    visibility?: boolean,   //Whether to display the automatic border detection icon. The default value is true.
    },
  funcConfirmExit: funcConfirmCropViewerExit,
 }

enum EnumDWT_ConfirmExitType = {
  Cancel: 0,
  Exit: 1,  //exit without saving
  SaveAndExit: 2,
};

function funcConfirmExit() {
  return true;  
}
function funcConfirmRemove () {
  return Promise.resolve(true);  
}

function funcConfirmCropViewerExit (bChanged, previousViewerName) {
	return Promise.resolve(EnumDWT_ConfirmExitType.Exit);
}

function funcConfirmExit(bChanged, previousViewerName) {
  return Promise.resolve(EnumDWT_ConfirmExitType.Exit);

function funcConfirmExitAfterSave(firedByDocumentEdit) {
	//DWObject.Addon.Camera.scanDocument() to continue capturing documents
}

```

**Availability**
<div class="availability">
<table>

<tr>
<td align="center">ActiveX</td>
<td align="center">H5(Windows)</td>
<td align="center">H5(macOS/TWAIN)</td>
<td align="center">H5(macOS/ICA)</td>
<td align="center">H5(Linux)</td>
<td align="center">WASM</td>
</tr>

<tr>
<td align="center">not supported</td>
<td align="center">not supported</td>
<td align="center">not supported</td>
<td align="center">not supported</td>
<td align="center">not supported</td>
<td align="center">v17.3+</td>
</tr>

</table>
</div>


