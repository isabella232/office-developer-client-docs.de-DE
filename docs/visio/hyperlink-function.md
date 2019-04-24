---
title: HYPERLINK-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navigiert zur angegebenen Adresse, die ein Datei-, UNC-oder URL-Pfad sein kann.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329946"
---
# <a name="hyperlink-function"></a>HYPERLINK Function

Navigiert zur angegebenen Adresse, die ein Datei-, UNC-oder URL-Pfad sein kann.
  
## <a name="syntax"></a>Syntax

Hyperlink ("* * *Address* * *" [, "* * unter *Adresse* * *", "* * *ExtraInfo* * *", * * *Fenster* * *, "* * *Frame* * *"]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _address_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein vollständiger Pfad oder ein relativer Pfad.  <br/> |
| _SubAddress_ <br/> |Optional  <br/> |**String** <br/> |Gibt eine Position innerhalb der Adresse an, zu der eine Verknüpfung hergestellt werden soll. Wenn address beispielsweise eine Microsoft Visio-Datei ist, kann unter Address ein Seiten Name sein; bei einer Microsoft Excel-Datei kann unter Adresse ein Arbeitsblatt oder ein Bereich innerhalb eines Arbeitsblatts sein. Wenn eine URL für eine HTML-Seite, unter Adresse kann eine Verankerung sein.  <br/> |
| _ExtraInfo_ <br/> |Optional  <br/> |**String** <br/> |Übergibt Informationen, die bei der Auflösung der URL verwendet werden, z. B. die Koordinaten für eine Imagemap.  <br/> |
| _Fenster_ <br/> |Optional  <br/> |**Boolean** <br/> |Legt fest, ob der Hyperlink in einem neuen Fenster geöffnet wird. Die Standardeinstellung lautet FALSE.  <br/> |
| _Rahmen_ <br/> |Optional  <br/> |**String** <br/> | Legt den Namen eines Frames zu einem Ziel fest, wenn Visio als aktives Dokument in einem ActiveX-Browser, z. B. Microsoft Internet Explorer 3.0 oder höher, geöffnet ist. Die Standardeinstellung ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn das Dokument keinen Basispfad besitzt, navigiert Visio relativ zum Dokumentpfad. Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert. 
  
Relative Pfade basieren auf dem Feld **Hyperlinkbasis**, das im Dialogfeld **Visio Eigenschaften** angegeben wird. 
  
Sie können die GOTOPAGE-Funktion nutzen, um zu den Zeichenblättern eines Dokuments zu navigieren. 
  
## <a name="example-1"></a>Beispiel 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Beispiel 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Beispiel 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Example 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

