---
title: QUEUEMARKEREVENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Bewirkt, dass die Anwendung ein Markerereignis für Ihr Add-On, Microsoft Visual Basic for Applications (VBA)-Code oder COM-Add-In löst.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418806"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT Function

Bewirkt, dass die Anwendung ein Markerereignis für Ihr Add-On, Microsoft Visual Basic for Applications (VBA)-Code oder COM-Add-In löst. 
  
## <a name="syntax"></a>Syntax

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zeichenfolge, die an den Ereignishandler übergeben werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die QUEUEMARKEREVENT-Funktion bietet Entwicklern die Möglichkeit, ihren Code über eine ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen zu übergeben. Wenn die Zelle, die die Formel mit der QUEUEMARKEREVENT-Funktion enthält, ausgewertet wird, wird von der Anwendung ein Markerereignis gesendet und  _event_string_ an alle Ereignishandler übergeben, die das **MarkerEvent-Ereignis** abhören. 
  
Weitere Informationen zu Markerereignissen finden Sie in den Themen **QueueMarkerEvent-Methode** und **MarkerEvent-Ereignis** in der Microsoft Visio Automation Reference. 
  
## <a name="example"></a>Beispiel

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten. 
  

