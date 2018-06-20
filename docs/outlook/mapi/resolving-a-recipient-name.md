---
title: Auflösen von Empfängernamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795384"
---
# <a name="resolving-a-recipient-name"></a>Auflösen von Empfängernamen

  
  
**Betrifft**: Outlook 
  
Wenn eine Nachricht adressiert ist, wird eine Empfängerliste mit Eigenschaften für jeden Empfänger erstellt. Durch die Zeit, den die Nachricht gesendet wird, muss eine der Eigenschaften des Empfängers langfristige Eintrags-ID sein: Um sicherzustellen, dass für jeden Empfänger die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft enthält, die [ADRLIST](adrlist.md) -Struktur, die zur Beschreibung der Empfängerliste in den Inhalt des Parameters _LpAdrList_ in einem Aufruf von [IAddrBook übergeben:: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** beginnt die Verarbeitung durch die Einträge in der **ADRLIST** -Struktur, die bereits behoben wurden, ignorieren, wie das Vorhandensein eines Bezeichners Eintrag in die entsprechenden [ADRENTRY](adrentry.md) Struktur **SPropValue** angegeben Array. Im nächsten Schritt weist **ResolveName** einmaligen-Eintragsbezeichner automatisch auf zwei Arten von Empfängern: 
  
- Empfänger mit einer Adresse, formatiert als eine IP-Adresse
    
- Empfänger mit einer Adresse formatiert wie folgt:
    
     `displayname[address type:email address]`
    
Für alle verbleibenden Einträge sucht **ResolveName** im Adressbuch nach einer genauen Übereinstimmung für den Anzeigenamen. **ResolveName** verwendet die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))-Eigenschaft, um die von Containern, Suche und die Suche Reihenfolge zu bestimmen. MAPI-Aufrufen die [IABContainer](iabcontainer-resolvenames.md) -Methode des jedes Container so versuchen Sie, alle Namen aufzulösen. Da einige Container nicht **ResolveNames**, unterstützt werden, wenn der Container MAPI_E_NO_SUPPORT zurückgibt, gilt MAPI eine eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) mit der Inhaltstabelle. Alle Address Book Container sind zur Unterstützung von namensauflösung mit diese Einschränkung erforderlich. Nachdem alle Namen aufgelöst werden, werden keine weiteren Container Aufrufe ausgeführt. Wenn alle Container aufgerufen wurde, aber nicht eindeutige oder nicht aufgelöste Namen bleiben, zeigt MAPI ein Dialogfeld Wenn möglich, den Benutzer zum Auflösen der verbleibenden Names an.
  
Die Einschränkung **PR_ANR** entspricht dem Wert der **PR_ANR** -Eigenschaft auf den Anzeigenamen der **ADRLIST** -Struktur. Beschränken die Ansicht des Containers Inhalt Tabelle mit der **PR_ANR** eigenschaftseinschränkung bewirkt, dass die Adressbuchanbieter zum Ausführen eines "am besten erraten" Typs der Übereinstimmung mit der Eigenschaft, die für den Anbieter sinnvoll-Suche. Beispielsweise könnte eine Adressbuchanbieter immer übereinstimmen Namen in der Empfängerliste gegen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) während einer anderen Administrator, um die Eigenschaft auswählen kann möglicherweise.
  
 **Um eine Beschränkung der PR_ANR-Eigenschaft für ein Adressbuchcontainer Inhaltstabelle festzulegen**
  
1. Erstellen Sie eine [SRestriction](srestriction.md) -Struktur, wie im folgenden Code dargestellt: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Rufen Sie den Inhalt der Tabelle [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, die **SRestriction** -Struktur als des _LpRestriction_ -Parameters übergeben. 
    

