---
title: HYPERLINK-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
ms.localizationpriority: medium
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navigiert zu der angegebenen Adresse, bei der es sich um einen Datei-, UNC- oder URL-Pfad handeln kann.
ms.openlocfilehash: 9443f30143a3beb19e31519d0dbe0845ddfd5451
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554705"
---
# <a name="hyperlink-function"></a>HYPERLINK Function

Navigiert zu der angegebenen Adresse, bei der es sich um einen Datei-, UNC- oder URL-Pfad handeln kann.
  
## <a name="syntax"></a>Syntax

HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein vollständiger Pfad oder ein relativer Pfad.  <br/> |
| _Unteradresse_ <br/> |Optional  <br/> |**String** <br/> |Gibt eine Position innerhalb von address an, mit der eine Verknüpfung hergestellt werden soll. Wenn es sich bei address beispielsweise um eine Microsoft Visio-Datei handelt, kann subaddress ein Zeichenblattname sein. Wenn es sich um eine Microsoft Excel-Datei handelt, kann subaddress ein Arbeitsblatt oder ein Arbeitsblattbereich sein. Wenn es sich um eine URL für eine HTML-Seite handelt, kann sich subaddress auf einen Anker beziehen.  <br/> |
| _Extrainfo_ <br/> |Optional  <br/> |**String** <br/> |Übergibt Informationen, die bei der Auflösung der URL verwendet werden, z. B. die Koordinaten für eine Imagemap.  <br/> |
| _Fenster_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |Legt fest, ob der Hyperlink in einem neuen Fenster geöffnet wird. Die Standardeinstellung lautet FALSE.  <br/> |
| _Rahmen_ <br/> |Optional  <br/> |**String** <br/> | Legt den Namen eines Frames zu einem Ziel fest, wenn Visio als aktives Dokument in einem ActiveX-Browser, z. B. Microsoft Internet Explorer 3.0 oder höher, geöffnet ist. Die Standardeinstellung ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das Dokument keinen Basispfad besitzt, navigiert Visio relativ zum Dokumentpfad. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert. 
  
Relative Pfade basieren auf dem Feld **Hyperlinkbasis**, das im Dialogfeld **Visio Eigenschaften** angegeben wird. 
  
Sie können die GOTOPAGE-Funktion nutzen, um zu den Zeichenblättern eines Dokuments zu navigieren. 
  
## <a name="example-1"></a>Beispiel 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Beispiel 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Beispiel 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Beispiel 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

