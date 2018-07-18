---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Gibt das Datum nach Jahr, Monat und Tag dargestellt entsprechend den Regionaleinstellungen des Systems kurzes Datumsformat formatiert. Die Werte für Jahr, Monat und Tag entsprechend der gregorianische Kalender.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796812"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Gibt das Datum, die durch *Year, Month* und *Day* entsprechend den Regionaleinstellungen des Systems kurzes Datumsformat formatiert. Die Werte für *Jahr*, *Monat* und *Tag* entsprechend der gregorianische Kalender. 
  
## <a name="syntax"></a>Syntax

Datum (** *Jahr* **, ** *Monat* **, ** *Tag* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Das Jahr.  <br/> |
| _Monat_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Monat.  <br/> |
| _day_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Tag.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

DATE(1999,6,7)
  
Gibt den Wert zurück, der 07.06.99 darstellt.
  
## <a name="example-2"></a>Beispiel 2

DATE(1999,6,7) + 4 t.
  
Gibt den Wert zurück, der 11.06.99 darstellt.
  
## <a name="example-3"></a>Beispiel 3

FORMAT(DATUM(1999,10,14),"C")
  
Gibt den Wert zurück, der Dienstag, 14. Oktober 1999 darstellt.
  

