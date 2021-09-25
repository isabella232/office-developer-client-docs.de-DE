---
title: PATHSEGMENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Gibt die 1-basierte Segmentnummer an der angegebenen Prozentmarke entlang des angegebenen Pfads zurück.
ms.openlocfilehash: 8ad574a112202c2f02fce3731a470960413d3042
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554215"
---
# <a name="pathsegment-function"></a>PATHSEGMENT Function

Gibt die 1-basierte Segmentnummer an der angegebenen Prozentmarke entlang des angegebenen Pfads zurück.
  
## <a name="syntax"></a>Syntax

PATHSEGMENT(** *section* **, ** *travel* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _reise_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Ganze Zahl
  

