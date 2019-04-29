---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436384"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht es den Formular Viewern, mit Formular Ansichts Kontexten und Formular Benachrichtigungen zu arbeiten, Formular Verben auszuführen und Formulare herunterzufahren.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularobjekte  <br/> |
|Implementiert von:  <br/> |Formularserver  <br/> |
|Aufgerufen von:  <br/> |Formular Betrachter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIForm  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SetViewcontext](imapiform-setviewcontext.md) <br/> |Richtet einen Ansichtskontext für das Formular ein.  <br/> |
|[GetViewcontext](imapiform-getviewcontext.md) <br/> |Gibt den aktuellen Ansichtskontext für das Formular zurück.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Schließt das Formular.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Fordert, dass das Formular alle Aufgaben ausführt, die es einem bestimmten Verb zuordnet.  <br/> |
|[Beraten](imapiform-advise.md) <br/> |Registriert einen Formular-Viewer für Benachrichtigungen zu Ereignissen, die das Formular betreffen.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Bricht eine Registrierung für Benachrichtigungen mit einem Formular Betrachter ab, der zuvor durch Aufrufen von **Advise**eingerichtet wurde.  <br/> |
|[Getlasterroraufzurufen](imapiform-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Form-Objekt auftritt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

