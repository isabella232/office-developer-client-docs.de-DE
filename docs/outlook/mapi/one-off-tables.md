---
title: One-Off Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439527"
---
# <a name="one-off-tables"></a>One-Off Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine einmal aufgeführte Tabelle enthält Informationen zu den Vorlagen, die ein Adressbuchanbieter zum Erstellen neuer Empfänger unterstützt. Einmaltabellen werden von Adressbuchanbietern, einzelnen Adressbuchcontainern und mapI implementiert und können dauerhaft oder temporär sein. 
  
> [!NOTE]
> Verwechseln Sie die Vorlagen in Einer-Aus-Tabellen nicht mit Vorlagenbezeichnern. Während ihre Zwecke ähnlich sind, sind ihre Codekonstrukte nicht gleich. Vorlagen werden verwendet, um Empfänger eines bestimmten Typs zu erstellen, während Vorlagenbezeichner verwendet werden, um die Daten eines Empfängers, der zu einem Hostanbieter gehört, mit Code zu binden, um einen anderen Empfänger zu unterstützen, der zu einem fremden Anbieter gehört. 
  
Clients erstellen neue Empfänger:
  
- So fügen Sie der Empfängerliste einer ausgehenden Nachricht hinzu.
    
- So fügen Sie einem der Container im Adressbuch hinzu.
    
In beiden Szenarien wird ein Adressbuchanbieter aufgefordert, eine einmal aufgeführte Tabelle zurück zu geben. Adressbuchanbieter können entweder eine einzelne einzelne Tabelle implementieren, die in beiden Situationen verwendet werden kann, oder eine eindeutige einmalige Tabelle für jede Situation. 
  
Wenn der Empfänger in eine ausgehende Nachricht eingeschlossen wird, ruft MAPI die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) des Adressbuchanbieters auf, um seine einmal aufgeführte Tabelle abzurufen. Die einmal aufgeführte Tabelle enthält Vorlagen, mit denen ein Benutzer Informationen eingeben kann, die zur Erstellung eines Empfängers mit einer gültigen Adresse führt. MAPI registriert sich für Benachrichtigungen in dieser Tabelle und hält sie offen, sodass Änderungen für den Benutzer widerspiegelt werden können. MAPI gibt die Tabelle nur frei, wenn die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Subsystems oder Adressbuchstatusobjekts aufgerufen wird. 
  
Wenn der Empfänger einem Container hinzugefügt wird, ruft MAPI einen anderen Aufruf ab und ruft die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, um seine **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft abzurufen. Der In dieser einmaltabelle enthaltene Vorlagensatz stellt die Typen von Empfängern dar, die dem Container hinzugefügt werden können. Beispielsweise wird auf E-Mail-Servern häufig ein Container für jedes installierte Gateway verfügbar gemacht, sodass jeder Container nur Adressen enthält, die für das entsprechende Gateway spezifisch sind.
  
MAPI stellt eine einzelne Tabelle bereit, die eigene Vorlagen sowie Vorlagen von jedem Adressbuchanbieter in der Sitzung enthält. MAPI stellt eine generische Vorlage zur Verfügung, mit der ein neuer Empfänger für jeden Adresstyp erstellt werden kann, vorausgesetzt, der Benutzer kennt sein Format. Adressbuchanbieter verwenden diese einmaltabelle, indem [sie IMAPISupport::GetOneOffTable aufrufen.](imapisupport-getoneofftable.md) Jede der in der EINMAL-TABELLE enthaltenen Vorlagen führt zur Erstellung von Empfängern mit gültigen Empfängeradressen.
  
Adressbuchanbieter bieten in der Regel eine Vorlage für jeden von ihnen unterstützten Adresstyp an. Die Unterstützung von Vorlagen ist jedoch nicht erforderlich. Adressbuchanbieter, die die Erstellung neuer Adressen nicht zulassen, können MAPI_E_NO_SUPPORT, wenn MAPI aufruft, um eine einmal aufgeführte Tabelle ananforderungs. Adressbuchanbieter, die die Erstellung neuer Adressen zulassen, aber keine Vorlagen angeben, können **IMAPISupport::GetOneOffTable** aufrufen, um die vorlagen zu verwenden, die in der einmal aufgeführten MAPI-Tabelle aufgeführt sind. 
  
Die folgenden Eigenschaften sind die erforderlichen Spalten, die in einmal festgelegten Tabellen festgelegt sind:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** gibt den Adresstyp an, der dem neuen Empfänger zugeordnet werden kann, der mit der Vorlage erstellt wurde. 
  
 **PR_DISPLAY_NAME** und **PR_DISPLAY_TYPE** dem neuen Empfänger Daten zuordnen. **PR_DISPLAY_NAME** enthält eine Zeichenzeichenfolge, die den neuen Empfänger identifiziert, und **PR_DISPLAY_TYPE** enthält eine Konstante, die den Typ des Symbols identifiziert, das mit der Zeile angezeigt werden soll. Vorlagen für Messagingbenutzer haben **ihre PR_DISPLAY_TYPE** auf DT_MAILUSER. Vorlagen für Verteilerlisten haben **ihre PR_DISPLAY_TYPE** auf DT_DISTLIST. 
  
 **PR_ENTRYID** ist der Eintragsbezeichner der Vorlage, die zum Erstellen eines neuen Empfängers verwendet werden soll. Diese Eintrags-ID kann an zukünftige [IAddrBook::NewEntry-,](iaddrbook-newentry.md) [IAddrBook::OpenEntry-](iaddrbook-openentry.md)und [IABContainer::CreateEntry-Aufrufe übergeben](iabcontainer-createentry.md) werden. Container legen die **PR_ENTRYID-Spalte** ihrer Zeile für die Standardbenutzervorlage für Messaging auf **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und die **PR_ENTRYID-Spalte** ihrer Zeile für die Standardvorlage für Verteilerlisten **auf PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) festgelegt. 
  
 **PR_DEPTH** wird verwendet, um die hierarchische Anzeige der Einträge in einer einzigen Tabelle zu unterstützen, indem die Einzugsebene für die Vorlage angegeben wird. Obwohl einzelne Tabellen entweder als flache Liste oder hierarchische Anzeige angezeigt werden können, ist letzteres vorzuziehen, und Adressbuchanbieter sollten dies unterstützen, indem sie die **spalte PR_DEPTH** für jede Zeile entsprechend festlegen. **PR_DEPTH** null basiert; Zeilen mit dem Wert 0 in der **PR_DEPTH** werden nicht eingezogen. Je höher der Wert **PR_DEPTH**, desto mehr wird die Zeile eingezogen. Beispielsweise werden Zeilen mit **PR_DEPTH** 1 eingezogen, während Zeilen mit  PR_DEPTH 3 eingezogen sind. 
  
 **PR_SELECTABLE** wird verwendet, um anzugeben, ob eine Zeile in der Tabelle eine Vorlage darstellt, die ausgewählt und zum Erstellen eines neuen Empfängers verwendet werden kann. Obwohl die meisten Zeilen in einer einmal erstellten Tabelle Vorlagen darstellen, können Anbieter Nichtvorlagenzeilen enthalten. Beispielsweise kann ein Anbieter die einmal verwendete Tabelle nach Vorlagentyp organisieren, einschließlich einer Kategoriezeile, die in der Anzeige angezeigt wird, aber nicht für die Empfängererstellung verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

