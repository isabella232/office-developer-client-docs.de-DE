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
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792274"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress: IUnknown

  
  
**Betrifft**: Outlook 
  
Implementiert eine Fortschritt-Objekt, das Clientanwendungen mit einer Statusanzeige bereitstellt. Eine Statusanzeige ist eine Benutzeroberfläche anzeigen, die den Prozentsatz der Fertigstellung eines Vorgangs, wie beispielsweise Kopieren von Ordnern zwischen Nachrichtenspeicher anzeigt. MAPI-und Clientanwendungen Implementieren des Fortschritts-Objekte und -Dienstanbieter verwenden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Fortschritt-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIProgress  <br/> |
|Zeigertyp:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, sobald sie zum Abschluss des Vorgangs vorgenommen wird.  <br/> |
|["GetFlags"](imapiprogress-getflags.md) <br/> |Gibt kennzeichnen Einstellungen aus dem Fortschritt-Objekt für die Ebene des Vorgangs auf die Fortschrittsinformationen berechnet werden.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Gibt die maximale Anzahl von Elementen in den Vorgang für den Fortschritt Informationen angezeigt werden.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Gibt den kleinsten Wert in der [SetLimits](imapiprogress-setlimits.md) -Methode für die Fortschritt Informationen angezeigt werden.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Legt die oberen und unteren Grenzwerten für die Anzahl der Elemente in den Vorgang und die Kennzeichen, die steuern, wie die Statusinformationen für den Vorgang berechnet wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

MAPI enthält einen _LpProgress_ -Parameter in vielen der Methoden, die möglicherweise langwierige Operationen ausführen.  _LpProgress_ verweist auf eine Clientimplementierung eines Fortschritt-Objekts. Clients, die die **IMAPIProgress** -Schnittstelle implementieren legen Sie diesen Parameter auf ihre Implementierung; Clients, die nicht **IMAPIProgress** implementieren festgelegt den Parameter auf NULL wurde. Um eine Statusanzeige während der Verarbeitung des Vorgangs anzuzeigen, verwenden Sie Dienstanbieter vom Client, falls verfügbar bereitgestellte Fortschritt-Objekts oder ein MAPI-Implementierung (angegeben ist, wenn _LpProgress_ auf NULL festgelegt ist). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Dateien**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiProgress.h und MapiProgress.cpp  <br/> |Nicht zutreffend  <br/> |Wenn die Einstellung IMAPIProgress aktiviert ist, wird MFCMAPI (engl.) eine Implementierung **IMAPIProgress** auf alle Funktionen, die aufruft, MFCMAPI (engl.) übergeben, die eine Implementierung akzeptieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Schnittstellen](mapi-interfaces.md)

