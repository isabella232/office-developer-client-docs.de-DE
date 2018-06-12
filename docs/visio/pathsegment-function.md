---
title: PATHSEGMENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Gibt die 1 basierende Segmentnummer an der angegebenen prozentmarkierung entlang des angegebenen Pfads zurück.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797609"
---
# <a name="pathsegment-function"></a>PATHSEGMENT Function

Gibt die 1 basierende Segmentnummer an der angegebenen prozentmarkierung entlang des angegebenen Pfads zurück.
  
## <a name="syntax"></a>Syntax

PATHSEGMENT (** *Abschnitt* **, ** *Reisen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Reisen_ <br/> |Erforderlich  <br/> |**Double** <br/> |Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Integer
  

