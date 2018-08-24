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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587131"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht das Formular Viewer Formular anzeigen Kontexten und Formular-Benachrichtigung zum Formular Verben ausführen und Herunterfahren Formulare entwickelt.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Formular-Objekte  <br/> |
|Implementiert von:  <br/> |Formular-Servern  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIForm  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Stellt ein Ansichtskontext für das Formular her.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Gibt den aktuellen Ansichtskontext für das Formular zurück.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Schließt das Formular.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Fordert, dass das Formular ausführen, was es Aufgaben ein bestimmtes Verb zugeordnet.  <br/> |
|[Beraten](imapiform-advise.md) <br/> |Registriert einen Formular-Viewer für Benachrichtigungen über Ereignisse, die Einfluss auf das Formular.  <br/> |
|[Heben Sie diesen Vorgang](imapiform-unadvise.md) <br/> |Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen der **Advise**hergestellt werden abgebrochen.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, der das Form-Objekt enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

