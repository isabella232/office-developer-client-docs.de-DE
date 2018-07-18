---
title: NEARESTPOINTONPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797535"
---
# <a name="nearestpointonpath-function"></a>NEARESTPOINTONPATH Function

Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

NEARESTPOINTONPATH (** *Abschnitt* **, ** *X* **, ** *y* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die _X_-Koordinate des angegebenen Punkts.  <br/> |
| _y_ <br/> |Erforderlich  <br/> |**Double** <br/> |Die _y_-Koordinate des angegebenen Punkts.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn _Section_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  

