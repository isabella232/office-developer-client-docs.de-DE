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
description: Führt String aus und übergibt die Befehlszeilenargumente für das Programm als Zeichenfolge.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797962"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS Function

Führt _String_ aus und übergibt die Befehlszeile _Argumente_ an die Anwendung als Zeichenfolge. 
  
## <a name="syntax"></a>Syntax

RUNADDONWARGS ("** *Zeichenfolge* **","** *Argumente* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name eines Add-Ons.  <br/> |
| _Argumente_ <br/> |Erforderlich  <br/> |**String** <br/> |Die an das Programm zu übergebenden Argumente.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In der Praxis sollten für _Arguments_ 50 oder weniger Zeichen werden. Verwenden der RUNADDONWARGS-Funktion ein Programm, wie ein Add-on, auf eine Zelle, eine Aktion oder Ereignisse Zelle einzubinden. 
  
Mit der RUNADDONWARGS-Funktion können nur Add-Ons ausgeführt werden, die Elemente der **Addons**-Auflistung der Anwendung sind. Add-Ons in dieser Auflistung müssen EXE- oder VSL-Dateien sein, für die Folgendes gilt: 
  
- Sie müssen im Verzeichnis **Startup** bzw. **Addons** der Anwendung installiert sein. 
    
- Sie müssen programmgesteuert mithilfe der **Add**-Methode der **Addons**-Auflistung hinzugefügt werden. 
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
In früheren Versionen von Visio wird diese Funktion in der Form _RUNADDONWARGS geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden.
  
## <a name="example"></a>Beispiel

RUNADDONWARGS ("GRAPHMKR. EXE-Datei"," / GraphMaker = Stack ") 
  
Führt das Add-On Graphmkr.exe aus und übergibt diesem das Argument /GraphMaker=Stack. 
  

