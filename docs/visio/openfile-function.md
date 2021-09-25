---
title: OPENFILE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
ms.localizationpriority: medium
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Öffnet ein Microsoft Visio-Dokument, falls es noch nicht geöffnet ist, und aktiviert das Dokumentfenster.
ms.openlocfilehash: f65309e28c102c8c222f16d164569d7e1b0f3924
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554334"
---
# <a name="openfile-function"></a>OPENFILE Function

Öffnet ein Microsoft Visio-Dokument, falls es noch nicht geöffnet ist, und aktiviert das Dokumentfenster.
  
## <a name="syntax"></a>Syntax

 **OPENFILE**( _"filename"_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Dateiname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Datei, einschließlich des Dateipfads, den Sie öffnen möchten.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es können mehrere OPENFILE-Funktionsaufrufe in eine Warteschlange gestellt und in einer ausgewerteten Reihenfolge ausgeführt werden. Falls das aktuelle Visio-Dokument für die visuelle Bearbeitung innerhalb einer anderen Anwendung geöffnet ist, wird eine neue Visio-Instanz mit dem angeforderten Dateinamen gestartet. 
  
Diese Funktion gibt immer FALSE zurück. 
  
In früheren Visio-Versionen wird diese Funktion in der Form _OPENFILE angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an. 
  
## <a name="example"></a>Beispiel

 `OPENFILE("C:/MyFile.vsdx")`
  
Öffnet die angegebene Datei "MyFile.vsdx" in einem neuen Fenster oder aktiviert das Fenster, wenn die Datei bereits geöffnet ist. 
  

