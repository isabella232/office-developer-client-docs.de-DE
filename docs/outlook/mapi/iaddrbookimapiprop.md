---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2edbc66be1f2f2ae761677c425616e70b77096d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561551"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf das MAPI-Adressbuch und umfasst Vorgänge wie das Anzeigen gängiger Dialogfelder. Öffnen von Containern, Messagingbenutzern und Verteilerlisten; und ausführen der Namensauflösung.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Adressbuchobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen, Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IAddrBook  <br/> |
|Zeigertyp:  <br/> |LPADRBOOK  <br/> |
|Transaktionsmodell:  <br/> |Schreibbar  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Öffnet einen Adressbucheintrag und gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf den Eintrag verwendet werden kann.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Adressbuchobjekt verweisen.  <br/> |
|[Beraten](iaddrbook-advise.md) <br/> |Registriert einen Client oder Dienstanbieter, um Benachrichtigungen über Änderungen an einem oder mehreren Einträgen im Adressbuch zu erhalten.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Bricht eine Benachrichtigungsregistrierung ab, die zuvor für einen Adressbucheintrag eingerichtet wurde.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Erstellt einen Eintragsbezeichner für eine einmalige Adresse.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Fügt einen neuen Empfänger zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Führt eine Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.  <br/> |
|[Adresse](iaddrbook-address.md) <br/> |Zeigt das Dialogfeld Outlook Adressbuch an.  <br/> |
|[Details](iaddrbook-details.md) <br/> |Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.  <br/> |
|**RecipOptions** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Gibt den Eintragsbezeichner des Containers zurück, der als persönliches Adressbuch (PAB) festgelegt ist.  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Legt einen bestimmten Container als persönliches Adressbuch (PAB) fest.  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Gibt den Eintragsbezeichner für den anfänglichen Adressbuchcontainer zurück.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Richtet den angegebenen Container als Standardadressbuchcontainer ein, der anfänglich zur Verfügung gestellt wird.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Gibt eine sortierte Liste der Eintragsbezeichner der Container zurück, die in den von der [ResolveName-Methode](iaddrbook-resolvename.md) initiierten Namensauflösungsprozess einbezogen werden sollen.  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Legt einen neuen Suchpfad im Profil fest, der für den Namensauflösungsprozess verwendet wird.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

