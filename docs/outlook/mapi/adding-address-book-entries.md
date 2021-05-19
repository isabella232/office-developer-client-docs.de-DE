---
title: Hinzufügen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421340"
---
# <a name="adding-address-book-entries"></a>Hinzufügen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Hinzufügen eines Messagingbenutzers oder einer Verteilerliste zu einem Container ruft ein Client [IAddrBook::NewEntry](iaddrbook-newentry.md) auf, oder ein Anbieter ruft [IMAPISupport::NewEntry](imapisupport-newentry.md) mit der Eintrags-ID des Zielcontainers im  _lpEIDContainer-Parameter_ auf. MAPI ruft wiederum die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des Containers auf, um den Eintrag mithilfe einer einmal erstellten Vorlage aus einer einmal erstellten Tabelle zu erstellen. Mit einer einmal erstellten Vorlage kann der Client einen neuen Empfänger eines bestimmten Typs erstellen. Die meisten Felder können bearbeitet werden. Die Vorlage, auf die der  _lpEntryID-Parameter_ verweist, kann eine Vorlage sein, die ihr Anbieter liefert, oder es kann sich um eine Vorlage eines fremden Anbieters, wenn Ihr Anbieter fremde Vorlagen unterstützt. Implementierungen von **CreateEntry** für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können, sind immer komplexer als Implementierungen für Anbieter, die dies nicht können. 
  
 **So implementieren Sie IABContainer::CreateEntry**
  
1. Bestimmen Sie den Typ des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird. 
    
2. Wenn der Eintragsbezeichner eine Vorlage für einen Messagingbenutzer, eine Verteilerliste oder einen Adressbuchcontainer darstellt, die sich im Besitz Ihres Anbieters befinden:
    
1. Erstellen und initialisieren Sie das entsprechende Objekt. Ihr Anbieter kann bei Bedarf einige anfängliche Eigenschaften festlegen. Diese Eigenschaften hängen vom Typ des zu erstellenden Empfängers ab. 
    
2. Gibt einen Zeiger auf die Implementierung des Objekts im Inhalt des  _lppMAPIPropEntry-Parameters_ zurück. 
    
3. Wenn der Eintragsbezeichner eine Vorlage für einen fremden Anbieter darstellt:
    
1. Rufen [Sie IMAPISupport::OpenEntry auf,](imapisupport-openentry.md) um das fremde Objekt zu öffnen. 
    
2. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts auf, übergeben Sie NULL für das Eigenschaftentagarray, um seine Eigenschaften abzurufen. 
    
3. Bearbeiten Sie das von **GetProps** zurückgegebene Eigenschaftswertarray, indem Sie das Eigenschaftstag in PR_NULL für alle Eigenschaften ändern, die nicht auf das neue Objekt angewendet werden und nicht übertragen werden sollten. 
    
4. Erstellen Sie einen Eintragsbezeichner für das neue Objekt. 
    
5. Erstellen Sie ein neues Objekt des entsprechenden Typs, entweder Messagingbenutzer oder Verteilerliste.
    
6. Initialisieren Sie das neue Objekt, indem Sie Standardeigenschaften festlegen.
    
7. Überprüfen Sie, ob das fremde Objekt die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. 
    
8. Wenn das fremde Objekt **PR_TEMPLATEID** unterstützt, rufen Sie [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) auf, um eine Eigenschaftsobjektschnittstelle vom fremden Anbieter abzurufen und den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des fremden Eigenschaftsobjekts zu setzen. 
    
9. Wenn das fremde Objekt keine **PR_TEMPLATEID,** legen Sie den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des neuen Objekts durch Ihren Anbieter. 
    
10. Rufen Sie [die IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Objekts auf, auf das der  _lppMAPIPropEntry-Parameter_ verweist, um die entsprechenden Eigenschaften aus dem fremden Objekt zu legen. 
    

