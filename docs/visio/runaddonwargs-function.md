---
title: RUNADDONWARGS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Führt Zeichenfolge aus und übergibt die Befehlszeilenargumente als Zeichenfolge an das Programm.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408705"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS Function

Führt  _Zeichenfolge_ aus und übergibt die  _Befehlszeilenargumente_ als Zeichenfolge an das Programm. 
  
## <a name="syntax"></a>Syntax

RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name eines Add-Ons.  <br/> |
| _Argumente_ <br/> |Erforderlich  <br/> |**String** <br/> |Die an das Programm zu übergebenden Argumente.  <br/> |
   
## <a name="remarks"></a>Hinweise

In der Praxis  _sollten Argumente_ 50 oder weniger Zeichen umfassen. Verwenden Sie die RUNADDONWARGS-Funktion, um ein Programm, z. B. ein Add-On, an eine Zelle zu binden, z. B. an eine Action- oder Event-Zelle. 
  
Mit der RUNADDONWARGS-Funktion können nur Add-Ons ausgeführt werden, die Elemente der **Addons**-Auflistung der Anwendung sind. Add-Ons in dieser Auflistung müssen EXE- oder VSL-Dateien sein, für die Folgendes gilt: 
  
- Sie müssen im Verzeichnis **Startup** bzw. **Addons** der Anwendung installiert sein. 
    
- Sie müssen programmgesteuert mithilfe der **Add**-Methode der **Addons**-Auflistung hinzugefügt werden. 
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
In früheren Versionen von Visio wird diese Funktion in der Form _RUNADDONWARGS geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.
  
## <a name="example"></a>Beispiel

RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack") 
  
Führt das Add-On Graphmkr.exe aus und übergibt diesem das Argument /GraphMaker=Stack. 
  

