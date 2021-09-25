---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d2f7bfd8c1bcc15cc12e4ab6efd26b0591f11b27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614024"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Greift auf Ressourcen in einem Adressbuchanbieter zu.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuchanmeldeobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABLogon  <br/> |
|Zeigertyp:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](iablogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Adressbuchanbieterfehler enthält.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Initiiert den Abmeldevorgang.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierungen zurück, um weiteren Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](iablogon-advise.md) <br/> |Registriert den Aufrufer, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Bricht Benachrichtigungen ab, die zuvor mit einem Aufruf der **Advise-Methode** eingerichtet wurden.  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Öffnet das Statusobjekt des Anbieters.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Öffnet einen Empfängereintrag mit Daten, die sich in einem Hostadressbuchanbieter befinden.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Allgemeine Informationen zu den Methoden der **IABLogon-Schnittstelle** finden Sie unter Implementieren der [Dienstanbieteranmeldung.](implementing-service-provider-logon.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

