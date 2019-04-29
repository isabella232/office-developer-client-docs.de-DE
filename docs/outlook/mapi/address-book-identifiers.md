---
title: Adressbuch Bezeichner
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
# <a name="address-book-identifiers"></a>Adressbuch Bezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Adressbuchanbieter weisen Eintrags-IDs mithilfe der **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft zu ihren Messaging-Benutzer-und Verteilerlisten Objekten zu. Client Anwendungen verwenden diese Eintragsbezeichner zum Öffnen und Zugreifen auf die Objekte, denen Sie zugeordnet sind.
  
Das Adressbuch verwendet drei andere Typen von Bezeichnern, um Objekte darzustellen:
  
- Bezeichner für Einmal-Einträge
    
- Einmalige Vorlagen Eintrags-IDs
    
- Vorlagenbezeichner
    
Aufgrund der Vielzahl von Eintrags Bezeichnern und der Ähnlichkeit, mit der Sie benannt wurden, ist es leicht zu verwechseln, wie die einzelnen Typen verwendet und erstellt werden. 
  
Ein einmaliger Eintragsbezeichner ist eine Eintrags-ID, die zum Öffnen und Zugreifen auf den Empfängertyp verwendet wird, der als einmaliger oder benutzerdefinierter Empfänger bezeichnet wird. Einmalig sind Empfänger, die keinem der Adressbuchanbieter im Profil angehören. Die den Einzel offs zugewiesenen Eintrags-IDs verwenden ein Format, das speziell für einmalige Empfänger reserviert ist. Da einmalige Eintrags-IDs zum Öffnen und Zugreifen auf Objekte verwendet werden, werden Sie in der PR_ENTRYID-Eigenschaft gespeichert.
  
Einmalige und einmalige Eintrags-IDs werden erstellt:
  
- Wenn Benutzer einer Clientanwendung einen Empfänger hinzufügen, der keinen Eintrag im Adressbuch zur Empfängerliste einer Nachricht darstellt.
    
- Wenn Benutzer einer Clientanwendung einen Empfänger hinzufügen, der keinen Eintrag im Adressbuch in einen änderbaren Adressbuchcontainer darstellt.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die nicht von dem zugehörigen Adressbuchanbieter bearbeitet werden kann.
    
- Wenn ein Transportanbieter eine Nachricht mit einer Adresse empfängt, die zu einem Gateway gehört.
    
In den ersten beiden Situationen ruft der Client **IAddrBook:: CreateOneOff** auf, um einen einmaligen Eintragsbezeichner mit dem neu erstellten einmaligen Empfänger zu verknüpfen. In den zweiten beiden Situationen ruft der Transportanbieter **IMAPISupport:: CreateOneOff** auf, um einen einmaligen Eintragsbezeichner mit der fremden Adresse zu verknüpfen. Weitere Informationen finden Sie unter [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md).
  
Ein einmaliger Vorlagen Eintragsbezeichner ist eine kurzfristige Eintrags-ID, die zum Öffnen und Zugreifen auf eine Vorlage zum Erstellen von einmaligen Einträgen verwendet wird. Sowohl Adressbuchanbieter als auch MAPI-Bereitstellungsvorlagen für die Eingabe der Informationen, die zum Erstellen eines Empfängers eines bestimmten Typs erforderlich sind. Informationen zu diesen Vorlagen, einschließlich ihrer Eintrags-IDs, werden in der einmaligen Tabelle veröffentlicht. Einmalige Tabellen werden angezeigt, wenn MAPI die **IABLogon:: GetOneOffTable** -Methode oder die **IMAPIProp:: OpenProperty** -Methode eines Adressbuch Containers zum Anfordern der **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md)) aufruft. -Eigenschaft oder wenn ein Anbieter **IMAPISupport:: GetOneOffTable**aufruft. Weitere Informationen finden Sie unter [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)und [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md).
  
Zum Erstellen einer neuen einmaligen Auswahl wählt ein Benutzer eine der in der einmaligen Tabelle aufgeführten Vorlagen aus. Der Client übergibt die PR_ENTRYID-Spalte aus der ausgewählten Zeile, die die ID des einmaligen Vorlagen Eintrags der ausgewählten Vorlage ist, an **IAddrBook:: upentry** im _lpEIDNewEntryTpl_ -Parameter. Weitere Informationen finden Sie unter [IAddrBook:: Reentry](iaddrbook-newentry.md). MAPI verwendet den einmaligen Vorlagen Eintragsbezeichner, um die Vorlage anzuzeigen und dem Benutzer die Eingabe der zum Erstellen des Empfängers erforderlichen Informationen zu ermöglichen. 
  
Ein Vorlagenbezeichner ist eine Eintrags-ID, die einige Adressbuchanbieter zusätzlich zur Eintrags-ID, die in der PR_ENTRYID-Eigenschaft aufbewahrt wird, ihren Empfängern zuweisen. Anbieter legen die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft eines Empfängers fest, um den Vorlagenbezeichner zu speichern. Einige Adressbuchanbieter weisen den gleichen Wert für die Eigenschaften der Vorlagen-ID und der Eintrags-ID eines Empfängers zu.
  
Vorlagenbezeichner werden nur von Adressbuch Anbietern und von MAPI verwendet, um Empfängerdaten in einem Anbieter, der als Hostanbieter bezeichnet wird, an Code für den Empfänger in einem anderen Anbieter zu binden, der als fremder Anbieter bezeichnet wird. Der Hostanbieter stellt den Speicher für den Empfänger bereit; der ausländische Anbieter liefert die Logik. Der Bindungsprozess ermöglicht einem Hostanbieter das Aktualisieren der Daten eines Empfängers, der mit dem Code eines fremden Anbieters gespeichert wird.
  
Wenn der Hostanbieter bereit ist, seinen Empfänger zu ändern, übergibt er die PR_TEMPLATEID-Eigenschaft in einem Aufruf an die **IMAPISupport::** opentemplatecollection-Methode, um den Bindungsprozess zu initiieren. MAPI setzt den Prozess fort, indem der Vorlagenbezeichner über einen Aufruf seiner **IABLogon:: OpenTemplate** -Methode an den entsprechenden fremden Anbieter übertragen wird. Weitere Informationen finden Sie unter [IMAPISupport::](imapisupport-opentemplateid.md) opentemplateserver und [IABLogon::](iablogon-opentemplateid.md)opentemplatecode. Der ausländische Anbieter gibt einen Zeiger auf seine **IMAPIProp** -Implementierung für den Empfänger zurück, den der Hostanbieter anstelle seiner eigenen Implementierung verwenden kann. 
  

