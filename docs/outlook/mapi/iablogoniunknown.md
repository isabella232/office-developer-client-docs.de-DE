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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791991"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Betrifft**: Outlook 
  
Greift auf Ressourcen in einer Adressbuchanbieter.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Address Book Logon-Objekten  <br/> |
|Implementiert von:  <br/> |Von adressbuchanbietern implementierte  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IABLogon  <br/> |
|Zeigertyp:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Address Book Anbieterfehler enthält.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Initiiert den Prozess abmelden.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Öffnet einen Container, messaging-Benutzer oder eine Verteilerliste, und gibt einen Zeiger auf eine Implementierung Zugriff zu ermöglichen.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.  <br/> |
|[Beraten](iablogon-advise.md) <br/> |Den Anrufer, um die Benachrichtigung der angegebenen Ereignisse, die einen Container, messaging-Benutzer oder Verteilerliste betreffen registriert.  <br/> |
|[Heben Sie diesen Vorgang](iablogon-unadvise.md) <br/> |Benachrichtigungen, die zuvor mit einem Aufruf der **Advise** -Methode eingerichtet wurden, werden abgebrochen.  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Öffnet den Anbieter Status-Objekt.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Öffnet einen Empfänger-Eintrag, der Daten in einer Host-Adressbuchanbieter hat.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern, die Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Allgemeine Informationen zu den Methoden der **IABLogon** -Schnittstelle finden Sie unter [Implementieren Service Provider Anmeldung](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

