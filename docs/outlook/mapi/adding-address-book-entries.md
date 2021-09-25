---
title: Hinzufügen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1a73a432511244726466e3717c58a085455baa18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605216"
---
# <a name="adding-address-book-entries"></a>Hinzufügen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Hinzufügen eines Messagingbenutzers oder einer Verteilerliste zu einem Container ruft ein Client [IAddrBook::NewEntry](iaddrbook-newentry.md) auf, oder ein Anbieter ruft [IMAPISupport::NewEntry](imapisupport-newentry.md) mit dem Eintragsbezeichner des Zielcontainers im  _lpEIDContainer-Parameter_ auf. MAPI ruft wiederum die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des Containers auf, um den Eintrag mithilfe einer einmaligen Vorlage aus einer einmaligen Tabelle zu erstellen. Mit einer einmaligen Vorlage kann der Client einen neuen Empfänger eines bestimmten Typs erstellen. Die meisten Felder können bearbeitet werden. Die Vorlage, auf die durch den  _LpEntryID-Parameter_ verwiesen wird, kann von Ihrem Anbieter bereitgestellt werden, oder es kann sich um eine Vorlage eines fremden Anbieters handelt, wenn Ihr Anbieter fremde Vorlagen unterstützt. Implementierungen von **CreateEntry** für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können, sind immer komplexer als Implementierungen für Anbieter, die dies nicht können. 
  
 **So implementieren Sie IABContainer::CreateEntry**
  
1. Bestimmen Sie den Typ des Eintragsbezeichners, der durch den  _lpEntryID-Parameter_ angegeben wird. 
    
2. Wenn der Eintragsbezeichner eine Vorlage für einen Messagingbenutzer, eine Verteilerliste oder einen Adressbuchcontainer im Besitz Ihres Anbieters darstellt:
    
1. Erstellen und initialisieren Sie das entsprechende Objekt. Ihr Anbieter kann bei Bedarf einige anfängliche Eigenschaften festlegen. Diese Eigenschaften hängen vom Typ des empfängers ab, der erstellt wird. 
    
2. Gibt einen Zeiger auf die Implementierung des Objekts im Inhalt des  _lppMAPIPropEntry-Parameters_ zurück. 
    
3. Wenn der Eintragsbezeichner eine Vorlage für einen fremden Anbieter darstellt:
    
1. Rufen Sie [IMAPISupport::OpenEntry](imapisupport-openentry.md) auf, um das fremde Objekt zu öffnen. 
    
2. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts auf, und übergeben Sie NULL für das Eigenschaftstagarray, um seine Eigenschaften abzurufen. 
    
3. Bearbeiten Sie das von **GetProps** zurückgegebene Eigenschaftenwertarray, indem Sie das Eigenschaftentag für alle Eigenschaften, die nicht für das neue Objekt gelten und nicht übertragen werden sollen, in PR_NULL ändern. 
    
4. Erstellen Sie einen Eintragsbezeichner für das neue Objekt. 
    
5. Erstellen Sie ein neues Objekt des entsprechenden Typs, entweder einen Messagingbenutzer oder eine Verteilerliste.
    
6. Initialisieren Sie das neue Objekt, indem Sie Standardeigenschaften festlegen.
    
7. Überprüfen Sie, ob das fremde Objekt die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. 
    
8. Wenn das fremde Objekt **PR_TEMPLATEID** unterstützt, rufen Sie [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) auf, um eine Eigenschaftsobjektschnittstelle vom fremdanbieter abzurufen und den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des fremden Eigenschaftsobjekts festzulegen. 
    
9. Wenn das fremde Objekt **PR_TEMPLATEID** nicht unterstützt, legen Sie den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des neuen Objekts durch den Anbieter fest. 
    
10. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Objekts auf, auf das der  _Parameter "lppMAPIPropEntry"_ verweist, um die entsprechenden Eigenschaften aus dem fremden Objekt festzulegen. 
    

