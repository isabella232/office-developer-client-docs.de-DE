---
title: Adressbuchbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421571"
---
# <a name="address-book-identifiers"></a>Adressbuchbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Adressbuchanbieter weisen ihren Messagingbenutzer- und Verteilerlistenobjekten mithilfe der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft Eintragsbezeichner zu. Clientanwendungen verwenden diese Eintragsbezeichner zum Öffnen und Zugreifen auf die Objekte, denen sie zugewiesen sind.
  
Das Adressbuch verwendet drei weitere Typen von Bezeichnern, um Objekte zu repräsentieren:
  
- Bezeichner für Einmal-Einträge
    
- Eindeutige Vorlageneintragsbezeichner
    
- Vorlagenbezeichner
    
Aufgrund der Vielzahl von Eintragsbezeichnern und der Ähnlichkeit, mit der sie benannt werden, ist es leicht zu verwechseln, wie jeder Typ verwendet und erstellt wird. 
  
Bei einer einmal verwendeten Eintrags-ID handelt es sich um eine Eintrags-ID, die zum Öffnen und Zugreifen auf den Empfängertyp verwendet wird, der als ein einmaler oder benutzerdefinierter Empfänger bezeichnet wird. Einmalempfänger sind Empfänger, die keinem der Adressbuchanbieter im Profil angehören. Die den Einmalempfängern zugewiesenen Eintragsbezeichner verwenden ein format, das speziell für einmal zugewiesene Empfänger reserviert ist. Da zum Öffnen und Zugreifen auf Objekte einmal verwendete Eintragsbezeichner verwendet werden, werden sie in der PR_ENTRYID gespeichert.
  
Es werden Einmal- und Einmaleintragsbezeichner erstellt:
  
- Wenn Benutzer einer Clientanwendung einen Empfänger hinzufügen möchten, der keinen Eintrag im Adressbuch zur Empfängerliste einer Nachricht repräsentiert.
    
- Wenn Benutzer einer Clientanwendung einen Empfänger hinzufügen möchten, der keinen Eintrag im Adressbuch zu einem veränderbaren Adressbuchcontainer repräsentiert.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die nicht von seinem zugehörigen Adressbuchanbieter verarbeitet werden kann.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die zu einem Gateway gehört.
    
In den ersten beiden Situationen ruft der Client **IAddrBook::CreateOneOff** auf, um dem neu erstellten einmal erstellten Empfänger einen einmal erstellten Eintragsbezeichner zuzuordnen. In den zweiten beiden Situationen ruft der Transportanbieter **IMAPISupport::CreateOneOff** auf, um der fremden Adresse eine eindeutige Eintrags-ID zuzuordnen. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Eine eindeutige Vorlageneintrags-ID ist eine kurzfristige Eintrags-ID, die zum Öffnen und Zugreifen auf eine Vorlage zum Erstellen von Einmalvorlagen verwendet wird. Sowohl Adressbuchanbieter als auch MAPI-Bereitstellungsvorlagen für die Eingabe der Informationen, die zum Erstellen eines Empfängers eines bestimmten Typs erforderlich sind. Informationen zu diesen Vorlagen, einschließlich ihrer Eintragsbezeichner, werden in der einmal aufgeführten Tabelle veröffentlicht. #A0 werden angezeigt, wenn MAPI entweder die **IABLogon::GetOneOffTable-Methode** oder die **IMAPIProp::OpenProperty-Methode** eines Adressbuchcontainers aufruft, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft an fordern oder wenn ein Anbieter **IMAPISupport::GetOneOffTable aufruft.** Weitere Informationen finden Sie unter [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)und [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Um eine neue Einmalvorlage zu erstellen, wählt ein Benutzer eine der in der Einmaltabelle aufgeführten Vorlagen aus. Der Client übergibt die PR_ENTRYID aus der ausgewählten Zeile, bei der es sich um die eindeutige Vorlageneintrags-ID der ausgewählten Vorlage handelt, an **IAddrBook::NewEntry** im _lpEIDNewEntryTpl-Parameter._ Weitere Informationen finden Sie unter [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI verwendet die id für den einmal erstellten Vorlageneintrag, um die Vorlage anzuzeigen und dem Benutzer die Eingabe der informationen zu ermöglichen, die zum Erstellen des Empfängers erforderlich sind. 
  
Ein Vorlagenbezeichner ist eine Eintrags-ID, die einige Adressbuchanbieter ihren Empfängern zusätzlich zu dem Eintragsbezeichner zuweisen, der in der eigenschaft PR_ENTRYID wird. Anbieter legen die Eigenschaft PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) eines Empfängers zum Speichern der Vorlagen-ID. Einige Adressbuchanbieter weisen denselben Wert für die Eigenschaften vorlagenbezeichner und eintragsbezeichner eines Empfängers zu.
  
Vorlagenbezeichner werden nur von Adressbuchanbietern und von MAPI verwendet, um Empfängerdaten in einem Anbieter, der als Hostanbieter bezeichnet wird, an Code für den Empfänger in einem anderen Anbieter zu binden, der als fremder Anbieter bezeichnet wird. Der Hostanbieter stellt den Speicher für den Empfänger zur Verfügung. Der fremde Anbieter liefert die Logik. Der Bindungsprozess ermöglicht es einem Hostanbieter, die Daten eines Empfängers zu aktualisieren, den er mithilfe des Codes eines fremden Anbieters speichert.
  
Wenn der Hostanbieter bereit ist, seinen Empfänger zu ändern, übergibt er die PR_TEMPLATEID-Eigenschaft in einem Aufruf an die **IMAPISupport::OpenTemplateID-Methode,** um den Bindungsprozess zu initiieren. MAPI setzt den Prozess fort, indem die Vorlagen-ID über einen Aufruf der **IABLogon::OpenTemplateID-Methode** an den entsprechenden fremden Anbieter übertragen wird. Weitere Informationen finden Sie unter [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) und [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). Der fremde Anbieter gibt einen Zeiger auf seine **IMAPIProp-Implementierung** für den Empfänger zurück, die der Hostanbieter an Stelle seiner eigenen Implementierung verwenden kann. 
  

