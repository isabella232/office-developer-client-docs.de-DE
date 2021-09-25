---
title: BOUNDINGBOXDIST-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 7a3da5917f38596ff3d277fc01d145752b6bda32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554817"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST Function

Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXDIST(** *Index* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Teil des umgebenden Felds des Shapes, der gemessen und zurückgegeben werden soll. Mögliche Werte finden Sie in den Hinweisen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>HinwBemerkungeneise

 *Index*  kann einer der folgenden Werte sein: 
  
|**Aspekt**|**Wert**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1  <br/> |
|Shape-Pin bis linke Kante  <br/> |2  <br/> |
|Shape-Pin bis rechte Kante  <br/> |3  <br/> |
|Shape-Pin bis obere Kante  <br/> |4   <br/> |
|Shape-Pin bis untere Kante  <br/> |5  <br/> |
|Mitte des umgebenden Felds bis PinX  <br/> |6   <br/> |
|Mitte des umgebenden Felds bis PinY  <br/> |7   <br/> |
   

