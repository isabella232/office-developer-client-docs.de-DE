---
title: Hinzufügen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: adbfbb73ac0f5f1e1cba547fa7a91393891fdb1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791251"
---
# <a name="adding-address-book-entries"></a>Hinzufügen von Adressbucheinträgen

  
  
**Betrifft**: Outlook 
  
Aufrufe [IMAPISupport::NewEntry](imapisupport-newentry.md) mit der Eintrags-ID des Zielcontainers in der _LpEIDContainer_ -Parameter einen Container, eine Client-Anrufe [IAddrBook::NewEntry](iaddrbook-newentry.md) oder einen Anbieter einen messaging Benutzer oder eine Verteilerliste hinzugefügt. MAPI-Aufrufen wiederum den Container [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um den Eintrag mithilfe einer einmaligen Vorlage aus einer einmaligen Tabelle zu erstellen. Eine einmalige Vorlage ermöglicht dem Client einen neuen Empfänger eines bestimmten Typs zu erstellen. Die meisten Felder können bearbeitet werden. Die Vorlage, auf das durch den Parameter _LpEntryID_ möglicherweise eine, die vom Dienstanbieter bereitstellt oder einer Vorlage von einem fremden Anbieter, wäre, wenn der Anbieter fremde Vorlagen unterstützt. Die Implementierung von **CreateEntry** für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können sind immer komplexer als Implementierungen für Anbieter, die nicht möglich. 
  
 **Implementieren von IABContainer::CreateEntry**
  
1. Bestimmen Sie den Typ des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
2. Wenn die Eintrags-ID eine Vorlage für eine messaging-Benutzer, Verteilerliste oder im Besitz des Anbieters Adressbuchcontainer darstellt:
    
1. Erstellen Sie und initialisieren Sie das entsprechende Objekt. Vom Dienstanbieter kann einige anfänglichen Eigenschaften festlegen, falls gewünscht. Diese Eigenschaften richten sich nach den Typ des zu erstellenden Empfänger. 
    
2. Ein Zeiger auf das Objekt Implementierung in den Inhalt des Parameters _LppMAPIPropEntry_ zurückgegeben. 
    
3. Wenn die Eintrags-ID eine Vorlage für einen fremden Anbieter darstellt:
    
1. Rufen Sie [IMAPISupport::OpenEntry](imapisupport-openentry.md) zum Öffnen des fremden Objekts. 
    
2. Rufen Sie das Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode übergeben NULL für die Arrays Tag-Eigenschaft, um seine Eigenschaften abzurufen. 
    
3. Bearbeiten des Eigenschaft Wertearrays von **GetProps** zurückgegeben, indem Sie das Eigenschafts-Tag auf PR_NULL für alle Eigenschaften, die nicht auf das neue Objekt angewendet und sollte nicht übertragen werden. 
    
4. Erstellen Sie einen Eintrag Bezeichner für das neue Objekt. 
    
5. Erstellen Sie ein neues Objekt der entsprechenden eingeben, entweder messaging Benutzer oder Verteilerliste aus.
    
6. Initialisieren Sie das neue Objekt durch Festlegen der Standardeigenschaften.
    
7. Überprüfen Sie, ob die fremden Objekts die Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. 
    
8. Wenn die fremden Objekts **PR_TEMPLATEID**unterstützt, rufen Sie [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) zum Abrufen einer Eigenschaft Objektschnittstelle aus der fremden Anbieter und Festlegen von den Inhalt des Parameters _LppMAPIPropEntry_ für die foreign-Eigenschaft objektimplementierung. 
    
9. Wenn die fremden Objekts **PR_TEMPLATEID**nicht unterstützt, legen Sie den Inhalt des Parameters _LppMAPIPropEntry_ an Ihren Anbieter die Implementierung des neuen Objekts. 
    
10. Rufen Sie die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode des Objekts auf das durch den Parameter _LppMAPIPropEntry_ , um die entsprechenden Eigenschaften aus der fremden Objekts festzulegen. 
    

