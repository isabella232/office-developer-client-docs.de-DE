---
title: QUEUEMARKEREVENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
ms.localizationpriority: medium
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Bewirkt, dass die Anwendung ein Markerereignis für Ihr Add-On, Ihren Microsoft Visual Basic for Applications (VBA)-Code oder ihr COM-Add-In auslöst.
ms.openlocfilehash: 66b00394897f45ed785e5f537d7bb32b2d2b544a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573656"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT Function

Bewirkt, dass die Anwendung ein Markerereignis für Ihr Add-On, Ihren Microsoft Visual Basic for Applications (VBA)-Code oder ihr COM-Add-In auslöst. 
  
## <a name="syntax"></a>Syntax

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zeichenfolge, die an den Ereignishandler übergeben werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die QUEUEMARKEREVENT-Funktion bietet Entwicklern die Möglichkeit, ihren Code über eine ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen zu übergeben. Wenn die Zelle mit der Formel mit der QUEUEMARKEREVENT-Funktion ausgewertet wird, löst die Anwendung ein Markerereignis aus und übergibt  _event_string_ an alle Ereignishandler, die auf das **MarkerEvent-Ereignis** lauschen. 
  
Weitere Informationen zu Markerereignissen finden Sie in den Themen zur **QueueMarkerEvent-Methode** und **zum MarkerEvent-Ereignis** in der Microsoft Visio Automation Reference. 
  
## <a name="example"></a>Beispiel

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten. 
  

