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
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429824"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf das MAPI-Adressbuch und enthält Vorgänge wie das Anzeigen allgemeiner Dialogfelder; Öffnen von Containern, Messaging Benutzern und Verteilerlisten; und durchführen der Namensauflösung.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuch Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen, Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAddrBook  <br/> |
|Zeigertyp:  <br/> |LPADRBOOK  <br/> |
|Transaktionsmodell:  <br/> |Nicht schreibbar  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Vergleicht zwei Eintrags-IDs, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Adressbuchobjekt verweisen.  <br/> |
|[Beraten](iaddrbook-advise.md) <br/> |Registriert einen Client oder Dienstanbieter für den Empfang von Benachrichtigungen zu Änderungen an einem oder mehreren Einträgen im Adressbuch.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Bricht eine zuvor für einen Adressbucheintrag eingerichtete Benachrichtigungs Registrierung ab.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Erstellt eine Eintrags-ID für eine einmalige Adresse.  <br/> |
|[NeuEintrag](iaddrbook-newentry.md) <br/> |Fügt einen neuen Empfänger zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Führt eine Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.  <br/> |
|[Adresse](iaddrbook-address.md) <br/> |Zeigt das Dialogfeld Outlook-Adressbuch an.  <br/> |
|[Details](iaddrbook-details.md) <br/> |Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.  <br/> |
|**RecipOptions** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Legt einen bestimmten Container als persönliches Adressbuch (PAB) fest.  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Gibt die Eintrags-ID für den anfänglichen Adressbuchcontainer zurück.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Legt den angegebenen Container als Standard-Adressbuchcontainer fest, der zunächst zur Verfügung gestellt wird.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Gibt eine sortierte Liste von Eintrags Bezeichnern der Container zurück, die in den von der ResolveName-Methode initiierten namens Auflösungsprozess eingeschlossen werden sollen. [](iaddrbook-resolvename.md)  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Legt einen neuen Suchpfad im Profil fest, der für den Prozess der Namensauflösung verwendet wird.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

