---
title: Einmaligen Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 3ad9141f2530e64664a2d0c75ece2b834cc6ad78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793290"
---
# <a name="one-off-tables"></a>Einmaligen Tabellen

**Betrifft**: Outlook 
  
Eine einmalige Tabelle enthält Informationen zu den Vorlagen, die ein Adressbuchanbieter zum Erstellen des neuen Empfänger unterstützt. Einmalige Tabellen von adressbuchanbietern implementierte, einzelne Adresse Adressbuch Container, und von MAPI implementiert werden und beständige oder temporäre werden können. 
  
> [!NOTE]
> Verwechseln Sie nicht die Vorlagen in einmaligen Tabellen mit Vorlage Bezeichnern; während ihre Zwecke ähnlich sind, sind ihre Codekonstrukte nichts gleichermaßen. Vorlagen werden verwendet, um die Empfänger eines bestimmten Typs erstellen, während die Vorlage-IDs verwendet werden, um die Daten des Empfängers ein, die mit einem Dienstanbieter Host mithilfe von Code zur Unterstützung von einem anderen Empfänger gehören, die zu einem fremden Anbieter gehören zu binden. 
  
Erstellen von neuen Empfänger Clients:
  
- Die Empfängerliste von ausgehenden Nachrichten hinzu.
    
- Um eine der Container im Adressbuch hinzuzufügen.
    
In beiden Szenarien wird ein Adressbuchanbieter gefragt, um einen einmaligen Tabelle zurückzugeben. Von adressbuchanbietern implementierte können entweder eine einzelne einmaligen Tabelle in sowohl Situationen verwendet werden oder eine eindeutige einmaligen Tabelle für jede Situation implementieren. 
  
Wenn der Empfänger eine ausgehende Nachricht enthalten sind, ruft MAPI der Adressbuchanbieter [GetOneOffTable](iablogon-getoneofftable.md) -Methode zum Abrufen der einmaligen Tabelle. Die einmalige Tabelle enthält Vorlagen, die einen Benutzer zur Eingabe von Informationen, die bei der Erstellung eines Empfängers mit einer gültigen Adresse resultierendes aktivieren. MAPI-Register für Benachrichtigungen in dieser Tabelle, halten ihn öffnen, damit Änderungen an den Benutzer widergespiegelt werden können. MAPI-Freigaben für die Tabelle nur, wenn seine Subsystem oder Adresse Adressbuch Status des Objekts [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode aufgerufen wird. 
  
Wenn der Empfänger zu einem Container hinzugefügt werden, wird durch MAPI eines anderen Anrufs Aufrufen des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Abrufen der Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Der Satz mit Vorlagen in dieser einmaligen Tabelle enthaltenen stellt die Typen von Empfängern an, die dem Container hinzugefügt werden können. Beispielsweise verfügbar machen, e-Mail-Servern häufig ein Container für jedes Gateway, das installiert werden, damit für jeden Container enthält nur die Adressen speziell für das entsprechende Gateway.
  
MAPI bietet einmalige Tabelle eine eigene Vorlagen sowie Vorlagen von jedem der adressbuchanbietern implementierte in der Sitzung enthält. MAPI bietet eine generische Vorlage, die verwendet werden kann, um einen neuen Empfänger für einen Adresstyp, vorausgesetzt, dass der Benutzer das Format weiß zu erstellen. Von adressbuchanbietern implementierte mithilfe dieser einmaligen Tabelle durch Aufrufen von [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Jede Vorlage in die MAPI-einmaligen Tabellenergebnisse bei der Erstellung von Empfängern mit gültigen Empfängeradressen enthalten.
  
Von adressbuchanbietern implementierte angeben in der Regel eine Vorlage für jede Adresstyp unterstützen. Unterstützung für Vorlagen ist nicht erforderlich, jedoch. Von adressbuchanbietern implementierte, die die Erstellung des neuen Adressen nicht zulassen zurückgeben MAPI_E_NO_SUPPORT, wenn MAPI-aufrufen, um einen einmaligen Tabelle anzufordern. Von adressbuchanbietern implementierte, die lässt das neue Adresse erstellen, aber keine Vorlagen bereit können **IMAPISupport::GetOneOffTable** , um die Vorlagen in der einmaligen MAPI-Tabelle aufgeführten verwenden aufrufen. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in einmaligen Tabellen festzulegen:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** gibt den Typ der Adresse, die mit den neuen Empfänger mit der Vorlage erstellte verknüpft werden kann. 
  
 **PR_DISPLAY_NAME** und **PR_DISPLAY_TYPE** zuordnen Daten den neuen Empfänger. **PR_DISPLAY_NAME** enthält eine Zeichenfolge, die den neuen Empfänger identifiziert und **PR_DISPLAY_TYPE** enthält eine Konstante, die den Typ der Zeile mit der anzuzeigende Symbol identifiziert. Vorlagen für die messaging-Benutzer haben ihre **PR_DISPLAY_TYPE** Spalte auf DT_MAILUSER festgelegt. Vorlagen für Verteilerlisten haben ihre **PR_DISPLAY_TYPE** Spalte auf DT_DISTLIST festgelegt. 
  
 **PR_ENTRYID** ist die Eintrags-ID der Vorlage, die zum Erstellen eines neuen Empfängers verwendet werden. Dieses Eintrags-ID kann in zukünftigen [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)und [IABContainer::CreateEntry](iabcontainer-createentry.md) aufrufen übergeben werden. Container legen Sie die Spalte **PR_ENTRYID** , der die Zeile für den Standard-messaging-Vorlage für Benutzer zu **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und der Spalte **PR_ENTRYID** ihre Zeile für die Standard-Verteilerliste Vorlage **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** wird verwendet, um die hierarchische Anzeige der Einträge in einer Tabelle einmaligen unterstützen, indem, die Einzugsebene für die Vorlage angibt. Obwohl einmalige Tabellen entweder als flache Liste oder einer hierarchischen Anzeige angezeigt werden können, da letztere ist vorzuziehen und adressbuchanbietern implementierte sollte durch Festlegen der **PR_DEPTH** -Spalte für jede Zeile entsprechend unterstützen. **PR_DEPTH** ist nullbasiert. Zeilen mit einem Wert von 0 in der Spalte **PR_DEPTH** sind nicht eingezogen. Je höher der Wert der **PR_DEPTH**, wird die weitere Zeile eingerückt. Beispielsweise sind Zeilen mit **PR_DEPTH** auf 1 gesetzt eingerückter eine Registerkarte Zeilen **PR_DEPTH** auf 3 festgelegt eingerückter drei Registerkarten. 
  
 **PR_SELECTABLE** wird verwendet, um anzugeben, ob eine Zeile in der Tabelle eine Vorlage darstellt, die ausgewählt und zum Erstellen eines neuen Empfängers verwendet werden können. Obwohl die meisten Zeilen in einer Tabelle einmaligen Vorlagen darstellen, können Anbieter ohne Vorlage Zeilen enthalten. Beispielsweise möchten ein Anbieter organisieren die einmalige Tabelle vom Typ Template, einschließlich einer Kategoriezeile, die in der Anzeige wird jedoch nicht für die Erstellung der Empfänger verwendet. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

