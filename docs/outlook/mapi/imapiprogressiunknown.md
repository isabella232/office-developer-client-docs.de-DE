---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d5756aca0afdbad732b09b4dc79d8b7e4c08021
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625574"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Statusobjekt, das Clientanwendungen eine Statusanzeige bereitstellt. Eine Statusanzeige ist eine Anzeige auf der Benutzeroberfläche, die den Prozentsatz des Abschlusses eines Vorgangs anzeigt, z. B. das Kopieren von Ordnern zwischen Nachrichtenspeichern. MAPI- und Clientanwendungen implementieren Fortschrittsobjekte, und Dienstanbieter verwenden diese. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |MAPI und Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProgress  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts beim Abschluss des Vorgangs.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Gibt Flageinstellungen aus dem Statusobjekt für die Vorgangsebene zurück, für die Statusinformationen berechnet werden.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Gibt die maximale Anzahl von Elementen in dem Vorgang zurück, für die Statusinformationen angezeigt werden.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Gibt den Minimalwert in der [SetLimits-Methode](imapiprogress-setlimits.md) zurück, für den Statusinformationen angezeigt werden.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Statusinformationen für den Vorgang berechnet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

MAPI enthält einen  _lpProgress-Parameter_ in vielen Methoden, die potenziell langwierige Vorgänge ausführen.  _lpProgress_ verweist auf eine Clientimplementierungen eines Statusobjekts. Clients, die die **IMAPIProgress-Schnittstelle** implementieren, legen diesen Parameter so fest, dass er auf ihre Implementierung verweist. Clients, die **IMAPIProgress** nicht implementieren, legen den Parameter auf NULL fest. Um während der Verarbeitung des Vorgangs eine Statusanzeige anzuzeigen, verwenden Dienstanbieter das vom Client bereitgestellte Statusobjekt (sofern verfügbar) oder eine MAPI-Implementierung (angegeben, wenn  _lpProgress_ auf NULL festgelegt ist). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Files**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiProgress.h und MapiProgress.cpp  <br/> |Nicht zutreffend  <br/> |Wenn die IMAPIProgress-Einstellung aktiviert ist, übergibt MFCMAPI eine **IMAPIProgress-Implementierung** an alle Funktionen, die MFCMAPI aufruft, die eine Implementierung akzeptieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

