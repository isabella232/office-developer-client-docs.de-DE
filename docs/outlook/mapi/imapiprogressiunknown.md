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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419646"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Statusobjekt, das Clientanwendungen eine Statusanzeige bietet. Ein Statusindikator ist eine Benutzeroberflächenanzeige, die den Prozentsatz des Abschlusses eines Vorgangs zeigt, z. B. das Kopieren von Ordnern zwischen Nachrichtenspeichern. MAPI- und Clientanwendungen implementieren Statusobjekte, und Dienstanbieter verwenden sie. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |MAPI- und Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProgress  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, der zum Abschluss des Vorgangs erfolgt.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Gibt Kennzeicheneinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der Fortschrittsinformationen berechnet werden.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Gibt die maximale Anzahl von Elementen im Vorgang zurück, für die Statusinformationen angezeigt werden.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Gibt den Minimalwert in der [SetLimits-Methode](imapiprogress-setlimits.md) zurück, für den Statusinformationen angezeigt werden.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

MAPI enthält einen  _lpProgress-Parameter_ in vielen Methoden, die potenziell langwierige Vorgänge ausführen.  _lpProgress_ verweist auf eine Clientimplementierung eines Progress-Objekts. Clients, die die **IMAPIProgress-Schnittstelle** implementieren, legen diesen Parameter fest, um auf ihre Implementierung zu verweisen. Clients, die **IMAPIProgress** nicht implementieren, legen den Parameter auf NULL fest. Zum Anzeigen eines Statusindikators während der Verarbeitung des Vorgangs verwenden Dienstanbieter das vom Client bereitgestellte Progress-Objekt( sofern verfügbar) oder eine MAPI-Implementierung (angegeben,  _wenn lpProgress_ auf NULL festgelegt ist). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Files**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiProgress.h und MapiProgress.cpp  <br/> |Nicht zutreffend  <br/> |Wenn die EINSTELLUNG IMAPIProgress aktiviert ist, übernimmt MFCMAPI eine **IMAPIProgress-Implementierung** an alle Funktionen, die MFCMAPI aufruft, die eine Implementierung akzeptieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

