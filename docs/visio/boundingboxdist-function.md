---
title: BOUNDINGBOXDIST-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796556"
---
# <a name="boundingboxdist-function"></a>BOUNDINGBOXDIST Function

Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010 
  
## <a name="syntax"></a>Syntax

BOUNDINGBOXDIST (** *Index* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Der Teil des das Shape umgebenden Felds um messen und zurückzukehren. Mögliche Werte finden Sie in den Hinweisen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Nummer**
  
## <a name="remarks"></a>Bemerkungen

 *Index* kann eine der folgenden Werte sein: 
  
|**Element**|**Wert**|
|:-----|:-----|
|Breite  <br/> |0  <br/> |
|Höhe  <br/> |1  <br/> |
|Shape-Pin bis linke Kante  <br/> |2  <br/> |
|Shape-Pin bis rechte Kante  <br/> |3  <br/> |
|Shape-Pin bis obere Kante  <br/> |4  <br/> |
|Shape-Pin bis untere Kante  <br/> |5  <br/> |
|Mitte des umgebenden Felds bis PinX  <br/> |6  <br/> |
|Mitte des umgebenden Felds bis PinY  <br/> |7  <br/> |
   

