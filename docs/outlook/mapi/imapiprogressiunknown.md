---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270077"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Progress-Objekt, das Clientanwendungen eine Statusanzeige bereitstellt. Eine Statusanzeige ist eine Benutzeroberflächenanzeige, die den Prozentsatz der Fertigstellung eines Vorgangs anzeigt, beispielsweise das Kopieren von Ordnern zwischen Nachrichten speichern. MAPI-und Clientanwendungen implementieren Progress-Objekte und Dienstanbieter verwenden Sie. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProgress  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts beim Abschließen des Vorgangs.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Gibt Flageinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der die Statusinformationen berechnet werden.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Gibt die maximale Anzahl von Elementen in dem Vorgang zurück, für die Statusinformationen angezeigt werden.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Gibt den kleinsten Wert in der [](imapiprogress-setlimits.md) setlimits-Methode zurück, für den Statusinformationen angezeigt werden.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente in dem Vorgang sowie die Flags fest, die Steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

MAPI enthält in vielen Methoden, die potenziell langwierige Vorgänge ausführen, einen _lpProgress_ -Parameter.  _lpProgress_ verweist auf eine Clientimplementierung eines Progress-Objekts. Clients, die die **IMAPIProgress** -Schnittstelle implementieren, legen diesen Parameter so fest, dass er auf die Implementierung verweist; Clients, die **IMAPIProgress** nicht implementieren, legen den Parameter auf NULL fest. Um während der Verarbeitung des Vorgangs eine Statusanzeige anzuzeigen, verwenden Dienstanbieter das vom Client bereitgestellte Progress-Objekt oder eine MAPI-Implementierung (angegeben, wenn _lpProgress_ auf NULL festgelegt ist). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Files**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiProgress. h und MapiProgress. cpp  <br/> |Nicht zutreffend  <br/> |Wenn die IMAPIProgress-Einstellung aktiviert ist, übergibt MFCMAPI eine **IMAPIProgress** -Implementierung an alle Funktionen, die MfcMapi aufrufen, die eine Implementierung akzeptieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

