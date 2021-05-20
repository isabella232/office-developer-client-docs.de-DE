---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431078"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zugriff auf Ressourcen in einem Adressbuchanbieter.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuchanmeldeobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABLogon  <br/> |
|Zeigertyp:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Adressbuchanbieterfehler enthält.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Initiiert den Abmeldevorgang.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Raten](iablogon-advise.md) <br/> |Registriert den Anrufer, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Benachrichtigungen, die zuvor mit einem Aufruf der **Advise-Methode eingerichtet wurden,** werden abgebrochen.  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Öffnet das Statusobjekt des Anbieters.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Öffnet einen Empfängereintrag mit Daten in einem Host-Adressbuchanbieter.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Gibt eine Tabelle mit einmal erstellten Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.  <br/> |
   
## <a name="remarks"></a>Hinweise

Allgemeine Informationen zu den Methoden der **IABLogon-Schnittstelle** finden Sie unter [Implementing Service Provider Logon](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

