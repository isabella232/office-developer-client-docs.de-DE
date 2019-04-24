---
title: Auflösen eines Empfängernamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328672"
---
# <a name="resolving-a-recipient-name"></a>Auflösen eines Empfängernamens

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht adressiert wird, wird eine Empfängerliste mit Eigenschaften für jeden Empfänger erstellt. Zu dem Zeitpunkt, zu dem die Nachricht gesendet wird, muss eine dieser Eigenschaften der langfristige Eintragsbezeichner des Empfängers sein. Um sicherzustellen, dass jeder Empfänger die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft enthält, übergeben Sie die [ADRLIST](adrlist.md) -Struktur, die ihre Empfängerliste in den Inhalten des _lpAdrList_ -Parameters beschreibt, in einem Aufruf von [IAddrBook:: ](iaddrbook-resolvename.md)ResolveName.
  
 **** ResolveName beginnt mit der Verarbeitung, indem die Einträge in der **ADRLIST** -Struktur, die bereits aufgelöst wurden, ignoriert werden, wie durch das vorhanden sein eines Eintrags Bezeichners in der **SPropValue** der zugehörigen [Miet](adrentry.md) Struktur angegeben. Array. Als nächstes **** weist ResolveName zwei Typen von Empfängern automatisch einmalige Eintrags-IDs zu: 
  
- Empfänger mit einer als Internet Adresse formatierten Adresse
    
- Empfänger mit einer Adresse, die wie folgt formatiert ist:
    
     `displayname[address type:email address]`
    
Für alle verbleibenden **** Einträge durchsucht ResolveName das Adressbuch nach einer genauen Übereinstimmung mit dem Anzeigenamen. **** ResolveName verwendet die **PR_AB_SEARCH_PATH** ([pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))-Eigenschaft, um den zu durchsuchenden Container Satz und die Suchreihenfolge zu bestimmen. MAPI Ruft die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode jedes Containers auf, um alle Namen aufzulösen. Da einige Container **ResolveNames**nicht unterstützen, wendet MAPI eine **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung für die Inhaltstabelle an, wenn der Container MAPI_E_NO_SUPPORT zurückgibt. Alle Adressbuchcontainer sind erforderlich, um die Namensauflösung mit dieser Einschränkung zu unterstützen. Nachdem alle Namen aufgelöst wurden, werden keine weiteren Container Aufrufe durchgeführt. Wenn alle Container aufgerufen wurden, aber mehrdeutige oder nicht aufgelöste Namen bleiben, zeigt MAPI ein Dialogfeld an, wenn möglich, um den Benutzer aufzufordern, die verbleibenden Namen aufzulösen.
  
Die **PR_ANR** -Einschränkung entspricht dem Wert der **PR_ANR** -Eigenschaft mit dem Anzeigenamen in der **ADRLIST** -Struktur. Durch Einschränken der Ansicht der Inhaltstabelle eines Containers mit der **PR_ANR** -Eigenschaftseinschränkung führt der Adressbuchanbieter einen "bestmöglichen" Suchtyp aus, der mit der für den Anbieter sinnvollsten Eigenschaft verglichen wird. Beispielsweise kann ein Adressbuchanbieter immer die Namen in der Empfängerliste mit **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) vergleichen, während eine andere Person es einem Administrator ermöglicht, die Eigenschaft auszuwählen.
  
 **So legen Sie eine PR_ANR-Eigenschaftseinschränkung für die Inhaltstabelle eines Adressbuch Containers fest**
  
1. Erstellen Sie eine [SRestriction](srestriction.md) -Struktur, wie im folgenden Code dargestellt: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Rufen Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode der Inhaltstabelle auf, und übergeben Sie die **SRestriction** -Struktur als _lpRestriction_ -Parameter. 
    

