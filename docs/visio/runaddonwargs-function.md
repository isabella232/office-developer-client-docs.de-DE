---
title: RUNADDONWARGS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
ms.localizationpriority: medium
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Führt eine Zeichenfolge aus und übergibt die Befehlszeilenargumente als Zeichenfolge an das Programm.
ms.openlocfilehash: 34de0d5024e761e9f8f0b4c39d3ed70e717a789e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573404"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS Function

Führt _eine Zeichenfolge_ aus und übergibt die Befehlszeilenargumente als Zeichenfolge an das Programm.  
  
## <a name="syntax"></a>Syntax

RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name eines Add-Ons.  <br/> |
| _Argumente_ <br/> |Erforderlich  <br/> |**String** <br/> |Die an das Programm zu übergebenden Argumente.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der Praxis sollten  _Argumente_ 50 oder weniger Zeichen enthalten. Verwenden Sie die RUNADDONWARGS-Funktion, um ein Programm, z. B. ein Add-On, an eine Zelle zu binden, z. B. an eine Zelle Action oder Events. 
  
Mit der RUNADDONWARGS-Funktion können nur Add-Ons ausgeführt werden, die Elemente der **Addons**-Auflistung der Anwendung sind. Add-Ons in dieser Auflistung müssen EXE- oder VSL-Dateien sein, für die Folgendes gilt: 
  
- Sie müssen im Verzeichnis **Startup** bzw. **Addons** der Anwendung installiert sein. 
    
- Sie müssen programmgesteuert mithilfe der **Add**-Methode der **Addons**-Auflistung hinzugefügt werden. 
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
In früheren Versionen von Visio wird diese Funktion in der Form _RUNADDONWARGS geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.
  
## <a name="example"></a>Beispiel

RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack") 
  
Führt das Add-On Graphmkr.exe aus und übergibt diesem das Argument /GraphMaker=Stack. 
  

