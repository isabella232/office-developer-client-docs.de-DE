---
title: OPENFILE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Öffnet ein Microsoft Visio-Dokument, wenn es noch nicht geöffnet ist, und das Dokumentfenster aktiviert.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797565"
---
# <a name="openfile-function"></a>OPENFILE Function

Öffnet ein Microsoft Visio-Dokument, wenn es noch nicht geöffnet ist, und das Dokumentfenster aktiviert.
  
## <a name="syntax"></a>Syntax

 **OPENFILE** ( _"Filename"_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Dateiname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Datei, einschließlich Dateipfad, den Sie öffnen möchten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es können mehrere OPENFILE-Funktionsaufrufe in eine Warteschlange gestellt und in einer ausgewerteten Reihenfolge ausgeführt werden. Falls das aktuelle Visio-Dokument für die visuelle Bearbeitung innerhalb einer anderen Anwendung geöffnet ist, wird eine neue Visio-Instanz mit dem angeforderten Dateinamen gestartet. 
  
Diese Funktion gibt immer FALSE zurück. 
  
In früheren Visio-Versionen wird diese Funktion in der Form _OPENFILE angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an. 
  
## <a name="example"></a>Beispiel

 `OPENFILE("C:/MyFile.vsdx")`
  
Öffnet die angegebene Datei "MyFile.vsdx" in einem neuen Fenster oder aktiviert das Fenster, wenn die Datei bereits geöffnet ist. 
  

