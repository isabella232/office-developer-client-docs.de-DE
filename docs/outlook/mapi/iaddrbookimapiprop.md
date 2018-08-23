---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579459"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf das MAPI-Adressbuch und enthält Vorgänge wie das allgemeine Dialogfelder anzeigen. Öffnen von Containern und messaging-Benutzer und Verteilerlisten; und namensauflösung ausführen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verfügbar gemacht von:  <br/> |Address Book-Objekten  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter-Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAddrBook  <br/> |
|Zeigertyp:  <br/> |LPADRBOOK  <br/> |
|Transaktionsmodell:  <br/> |Nicht geschrieben  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Öffnet ein Adressbuch Adresseintrag, und gibt einen Zeiger auf eine Schnittstelle, die den Eintrag Zugriff auf verwendet werden kann.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, die gehören zu einer bestimmten Adressbuchanbieter um festzustellen, ob diese auf das gleiche Address Book-Objekt verweisen.  <br/> |
|[Beraten](iaddrbook-advise.md) <br/> |Registriert einen Client oder Dienstanbieter Erhalt von Benachrichtigungen zu Änderungen an einen oder mehrere Einträge im Adressbuch an.  <br/> |
|[Heben Sie diesen Vorgang](iaddrbook-unadvise.md) <br/> |Benachrichtigungsregistrierung eines für einen Adresseintrag Adressbuch zuvor eingerichtet werden abgebrochen.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Fügt einen neuen Empfänger um eine Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Führt Namensresolution Eintragsbezeichner an Empfänger in der Empfängerliste zuweisen.  <br/> |
|[Adresse](iaddrbook-address.md) <br/> |Zeigt das Dialogfeld Adressbuch von Outlook-Adresse an.  <br/> |
|[Details](iaddrbook-details.md) <br/> |Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.  <br/> |
|**RecipOptions** <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Gibt die Eintrags-ID des Containers, die als das persönliche Adressbuch (PAB) festgelegt ist.  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Legt einen bestimmten Container als das persönliche Adressbuch (PAB) fest.  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Gibt die Eintrags-ID für die anfängliche Adressbuchcontainer zurück.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Richtet den angegebenen Container als Standard-Adressbuchcontainer, die Anfangs verfügbar gemacht wird.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Gibt eine geordnete Liste von Eintrags-IDs der Container in der [ResolveName](iaddrbook-resolvename.md) -Methode initiiert Vorgang der Lösung enthalten sein.  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Legt einen neuen Pfad für die Suche in das Profil, das für den Vorgang der Lösung verwendet wird.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

