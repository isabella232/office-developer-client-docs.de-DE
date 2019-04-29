---
title: BOUNDINGBOXDIST-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428277"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST Function

Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXDIST (* * *Index* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Teil des umgebenden Felds des Shapes, der gemessen und zurückgegeben werden soll. Mögliche Werte finden Sie in den Hinweisen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>Bemerkungen

 *Index* kann einer der folgenden Werte sein. 
  
|**Item**|**Wert**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1  <br/> |
|Shape-Pin bis linke Kante  <br/> |2  <br/> |
|Shape-Pin bis rechte Kante  <br/> |3  <br/> |
|Shape-Pin bis obere Kante  <br/> |4  <br/> |
|Shape-Pin bis untere Kante  <br/> |5  <br/> |
|Mitte des umgebenden Felds bis PinX  <br/> |6  <br/> |
|Mitte des umgebenden Felds bis PinY  <br/> |7  <br/> |
   

