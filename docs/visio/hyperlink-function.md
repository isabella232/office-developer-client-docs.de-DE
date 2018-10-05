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
description: Navigiert zu der angegebenen Adresse, eine Datei, UNC oder URL sein kann Pfad.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401076"
---
# <a name="hyperlink-function"></a>HYPERLINK Function

Navigiert zu der angegebenen Adresse, eine Datei, UNC oder URL sein kann Pfad.
  
## <a name="syntax"></a>Syntax

HYPERLINK ("** *Adresse* **" [,"** *Subaddress* **","** *Extrainfo* **", ** *Fenster* **, "** *Frame* **"]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Adresse_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein vollständiger Pfad oder ein relativer Pfad.  <br/> |
| _SubAddress_ <br/> |Optional  <br/> |**String** <br/> |Gibt eine Position innerhalb von address an, mit der eine Verknüpfung hergestellt werden soll. Wenn es sich bei address beispielsweise um eine Microsoft Visio-Datei handelt, kann subaddress ein Zeichenblattname sein. Wenn es sich um eine Microsoft Excel-Datei handelt, kann subaddress ein Arbeitsblatt oder ein Arbeitsblattbereich sein. Wenn es sich um eine URL für eine HTML-Seite handelt, kann sich subaddress auf einen Anker beziehen.  <br/> |
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
  
## <a name="example-4"></a>Beispiel 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

