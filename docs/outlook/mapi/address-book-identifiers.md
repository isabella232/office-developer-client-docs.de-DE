---
title: Adressbuchbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f312f07386b74a58e6da814191c8b67a667e9fbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572130"
---
# <a name="address-book-identifiers"></a>Adressbuchbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Adressbuchanbieter weisen ihren Nachrichtenbenutzer- und Verteilerlistenobjekten Eintragsbezeichner mithilfe der **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) zu. Clientanwendungen verwenden diese Eintragsbezeichner, um die Objekte zu öffnen und darauf zuzugreifen, denen sie zugewiesen sind.
  
Das Adressbuch verwendet drei andere Arten von Bezeichnern zur Darstellung von Objekten:
  
- Bezeichner für Einmal-Einträge
    
- Bezeichner für einmalige Vorlageneingabe
    
- Vorlagenbezeichner
    
Aufgrund der Vielzahl von Eintragsbezeichnern und der Ähnlichkeit, mit der sie benannt werden, ist es leicht zu verwechseln, wie die einzelnen Typen verwendet und erstellt werden. 
  
Ein einmaliger Eintragsbezeichner ist ein Eintragsbezeichner, der zum Öffnen und Zugreifen auf den Empfängertyp verwendet wird, der als einmaliger oder benutzerdefinierter Empfänger bezeichnet wird. Einmalige Empfänger sind Empfänger, die keinem der Adressbuchanbieter im Profil angehören. Die Eintragsbezeichner, die einmaligen Empfängern zugewiesen sind, verwenden ein Speziell für einmalige Empfänger reserviertes Format. Da einmalige Eintragsbezeichner zum Öffnen und Zugreifen auf Objekte verwendet werden, werden sie in der PR_ENTRYID-Eigenschaft gespeichert.
  
Einmalige und einmalige Eintragsbezeichner werden erstellt:
  
- Wenn Benutzer einer Clientanwendung entscheiden, einen Empfänger hinzuzufügen, der keinen Eintrag im Adressbuch zur Empfängerliste einer Nachricht darstellt.
    
- Wenn Benutzer einer Clientanwendung entscheiden, einen Empfänger hinzuzufügen, der keinen Eintrag im Adressbuch zu einem modifizierbaren Adressbuchcontainer darstellt.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die von seinem zugehörigen Adressbuchanbieter nicht verarbeitet werden kann.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die zu einem Gateway gehört.
    
In den ersten beiden Situationen ruft der Client **IAddrBook::CreateOneOff** auf, um dem neu erstellten einmaligen Empfänger einen einmaligen Eintragsbezeichner zuzuordnen. In den zweiten beiden Situationen ruft der Transportanbieter **IMAPISupport::CreateOneOff** auf, um der Fremdadresse einen einmaligen Eintragsbezeichner zuzuordnen. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Ein einmaliger Vorlageneintragsbezeichner ist ein kurzfristiger Eintragsbezeichner, der zum Öffnen und Zugreifen auf eine Vorlage zum Erstellen von Einmaligen verwendet wird. Sowohl Adressbuchanbieter als auch MAPI-Bereitstellungsvorlagen für die Eingabe der Informationen, die zum Erstellen eines Empfängers eines bestimmten Typs erforderlich sind. Informationen zu diesen Vorlagen, einschließlich der eintragsbezeichner, werden in der einmaligen Tabelle veröffentlicht. Einmalige Tabellen werden angezeigt, wenn MAPI entweder die **IABLogon::GetOneOffTable-Methode** oder die **IMAPIProp::OpenProperty-Methode** eines Adressbuchcontainers aufruft, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft anzufordern, oder wenn ein Anbieter **IMAPISupport::GetOneOffTable aufruft.** Weitere Informationen finden Sie unter [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)und [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Um eine neue Einmalige zu erstellen, wählt ein Benutzer eine der Vorlagen aus, die in der einmaligen Tabelle aufgeführt sind. Der Client übergibt die PR_ENTRYID Spalte aus der ausgewählten Zeile, bei der es sich um den einmaligen Vorlageneintragsbezeichner der ausgewählten Vorlage handelt, an **IAddrBook::NewEntry** im _LpEIDNewEntryTpl-Parameter._ Weitere Informationen finden Sie unter [IAddrBook::NewEntry](iaddrbook-newentry.md). DIE MAPI verwendet den einmaligen Vorlageneintragsbezeichner, um die Vorlage anzuzeigen und dem Benutzer die Eingabe der zum Erstellen des Empfängers erforderlichen Informationen zu ermöglichen. 
  
Ein Vorlagenbezeichner ist ein Eintragsbezeichner, den einige Adressbuchanbieter ihren Empfängern zusätzlich zu dem Eintragsbezeichner zuweisen, der in der PR_ENTRYID-Eigenschaft beibehalten wird. Anbieter legen die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) eines Empfängers fest, um den Vorlagenbezeichner zu speichern. Einige Adressbuchanbieter weisen denselben Wert für die Vorlagenbezeichner- und Eintragsbezeichnereigenschaften eines Empfängers zu.
  
Vorlagenbezeichner werden nur von Adressbuchanbietern und von MAPI verwendet, um Empfängerdaten in einem Anbieter, der als Hostanbieter bezeichnet wird, an Code für den Empfänger in einem anderen Anbieter zu binden, der als fremder Anbieter bezeichnet wird. Der Hostanbieter stellt den Speicher für den Empfänger bereit. der fremde Anbieter stellt die Logik bereit. Der Bindungsprozess ermöglicht es einem Hostanbieter, die Daten eines Empfängers, den er speichert, mithilfe des Codes eines fremden Anbieters zu aktualisieren.
  
Wenn der Hostanbieter bereit ist, seinen Empfänger zu ändern, übergibt er die PR_TEMPLATEID-Eigenschaft in einem Aufruf an die **IMAPISupport::OpenTemplateID-Methode,** um den Bindungsprozess zu initiieren. MAPI setzt den Vorgang fort, indem der Vorlagenbezeichner über einen Aufruf der **IABLogon::OpenTemplateID-Methode** an den entsprechenden fremdanbieter übertragen wird. Weitere Informationen finden Sie unter [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) und [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). Der fremde Anbieter gibt einen Zeiger auf seine **IMAPIProp-Implementierung** für den Empfänger zurück, die der Hostanbieter anstelle seiner eigenen Implementierung verwenden kann. 
  

