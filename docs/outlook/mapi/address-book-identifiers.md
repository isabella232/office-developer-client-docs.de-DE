---
title: -Adressbuch Adress-IDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0814d76dac97e40940f41c49dbf72efdd26b3cca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791264"
---
# <a name="address-book-identifiers"></a>-Adressbuch Adress-IDs

  
  
**Betrifft**: Outlook 
  
Alle von adressbuchanbietern implementierte weisen Eintragsbezeichner mithilfe der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft auf die messaging-Benutzer und Verteilung List-Objekten. Clientanwendungen verwenden diese Eintragsbezeichner zum Öffnen und Zugreifen auf die Objekte, die sie zugeordnet sind.
  
Das Adressbuch nutzt drei anderen Arten von Bezeichnern Objekte dargestellt:
  
- Einmaligen-Eintragsbezeichner
    
- Einmaligen Vorlage-Eintragsbezeichner
    
- Vorlage-IDs
    
Wegen der Vielzahl von Eintrags-IDs und der Ähnlichkeit, mit der sie benannt werden, ist es einfach zu wissen, wie jeder Typ verwendet und erstellt wird. 
  
Eine einmalige Eintrags-ID ist eine Eintrags-ID, die zum Öffnen und Zugreifen auf den Typ der Empfänger einer einmaligen genannt, oder einen benutzerdefinierten Empfänger verwendet wird. Fly sind Empfänger, die nicht an die adressbuchanbietern implementierte im Profil gehören. Die zugewiesenen Fly Eintragsbezeichner verwenden Sie ein Format speziell reserviert für einmaligen Empfänger. Da einmaligen-Eintragsbezeichner öffnen und Zugreifen auf Objekte verwendet werden, werden sie in der PR_ENTRYID-Eigenschaft gespeichert.
  
Fly und einmaligen-Eintragsbezeichner werden erstellt:
  
- Wenn Benutzer von einer Clientanwendung aus einstellen, einen Empfänger hinzuzufügen, der keine Einträge im Adressbuch an eine Nachricht Empfängerliste darstellt.
    
- Wenn Benutzer von einer Clientanwendung aus einstellen, einen Empfänger hinzuzufügen, der alle Einträge im Adressbuch nicht um eine änderbare Adressbuchcontainer darstellt.
    
- Wenn ein Transportdienstes eine Nachricht mit einer Adresse erhält, die von der zugehörigen Adressbuchanbieter bearbeitet werden kann.
    
- Wenn ein Transportdienstes eine Nachricht mit einer Adresse erhält, die ein Gateway angehört.
    
In den ersten beiden Situationen ruft der Client **IAddrBook::CreateOneOff** um einen einmaligen Eintrags-ID der neu erstellten einmaligen Empfänger zuzuordnen. In den beiden Situationen ruft der Adressbuchhierarchie **IMAPISupport::CreateOneOff** um einen einmaligen Eintrags-ID der fremde Adresse zuzuordnen. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Eine einmalige Vorlage Eintrags-ID ist eine kurzfristige Eintrags-ID, die zum Öffnen und Zugreifen auf eine Vorlage zum Erstellen von Fly verwendet wird. Geben adressbuchanbietern implementierte und MAPI-Vorlagen für die Eingabe von Informationen, die zum Erstellen eines Empfängers eines bestimmten Typs erforderlich ist. Informationen zu diesen Vorlagen, einschließlich ihrer Eintragsbezeichner wird in der einmaligen Tabelle veröffentlicht. Einmalige Tabellen werden angezeigt, wenn MAPI-aufrufen, die **GetOneOffTable** -Methode oder einer Adressbuchcontainer **IMAPIProp::OpenProperty** -Methode an die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) Eigenschaft oder wenn ein Anbieter **IMAPISupport::GetOneOffTable**aufruft. Weitere Informationen finden Sie unter [GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)und [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Zum Erstellen einer neuen einmaligen wählt ein Benutzer eine der Vorlagen in der einmaligen Tabelle aufgeführt. Der Client übergibt die PR_ENTRYID Spalte aus der ausgewählten Zeile, die der einmaligen Vorlage Eintrags-ID der ausgewählten Vorlage ist, an **IAddrBook::NewEntry** im _LpEIDNewEntryTpl_ -Parameter. Weitere Informationen finden Sie unter [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI verwendet die einmaligen Vorlage Eintrags-ID aus, um die Vorlage anzuzeigen und den Benutzer zur Eingabe dieser Informationen zum Erstellen des Empfängers benötigt erlauben. 
  
Ein Vorlagenbezeichner ist eine Eintrags-ID, die den Empfängern zusätzlich zu den Eintrag Bezeichner einige adressbuchanbietern implementierte zuweisen, die in der Eigenschaft PR_ENTRYID gehalten wird. Anbieter legen Sie einen Empfänger **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des Bezeichners Vorlage gespeichert. Einige adressbuchanbietern implementierte weisen den gleichen Wert für die Vorlagenbezeichner des Empfängers und Eintrag Bezeichnereigenschaften.
  
Vorlage-IDs werden nur von adressbuchanbietern implementierte und MAPI zum Binden von Daten des Empfänger in einem Anbieter verwendet, als Hostanbieter auf, um den Code für den Empfänger in einen anderen Anbieter bezeichnet, als der fremde Anbieter bezeichnet. Hostanbieter liefert den Speicher für den Empfänger an. der fremde Anbieter stellt die Logik. Die Bindung aktiviert ein Hostanbieter so aktualisieren Sie die Daten eines Empfängers, dass sie mit dem Code eines fremden Anbieters speichert.
  
Wenn der Hostanbieter bereit zum Ändern der Empfänger ist, übergibt sie die PR_TEMPLATEID-Eigenschaft in einem Aufruf der **IMAPISupport::OpenTemplateID** -Methode der Bindung zu initiieren. MAPI wird der Vorgang fortgesetzt, indem der Vorlagenbezeichner an den entsprechenden fremden Anbieter durch einen Aufruf der Methode **OpenTemplateID** übertragen. Weitere Informationen finden Sie unter [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) und [OpenTemplateID](iablogon-opentemplateid.md). Der fremde Anbieter gibt einen Zeiger auf seine Implementierung **IMAPIProp** für den Empfänger, die Hostanbieter anstelle einer eigenen Implementierung verwenden können. 
  

