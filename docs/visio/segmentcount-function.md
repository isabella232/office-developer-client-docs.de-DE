---
title: SEGMENTCOUNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.
ms.openlocfilehash: 0250c6c9a88f1de121a5cd8e930158203537c229
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553935"
---
# <a name="segmentcount-function"></a>SEGMENTCOUNT Function

Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.
  
## <a name="syntax"></a>Syntax

SEGMENTCOUNT(** *pathRef* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf die Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Liniensprünge sind in der Gesamtzahl der zurückgegebenen Segmente nicht eingeschlossen.
  

