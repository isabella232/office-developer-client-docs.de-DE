---
title: One-Off Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 0dfa967569a276c1a2f11248b0a166be21c4ac0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595630"
---
# <a name="one-off-tables"></a>One-Off Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine einmalige Tabelle enthält Informationen zu den Vorlagen, die ein Adressbuchanbieter zum Erstellen neuer Empfänger unterstützt. Einmalige Tabellen werden von Adressbuchanbietern, einzelnen Adressbuchcontainern und mapi implementiert und können dauerhaft oder temporär sein. 
  
> [!NOTE]
> Verwechseln Sie die Vorlagen in einmaligen Tabellen nicht mit Vorlagenbezeichnern. Obwohl ihre Zwecke ähnlich sind, sind ihre Codekonstrukte nichts gleich. Vorlagen werden verwendet, um Empfänger eines bestimmten Typs zu erstellen, während Vorlagenbezeichner verwendet werden, um die Daten eines Empfängers zu binden, der zu einem Hostanbieter gehört, mit Code zur Unterstützung eines anderen Empfängers, der zu einem fremden Anbieter gehört. 
  
Clients erstellen neue Empfänger:
  
- So fügen Sie der Empfängerliste einer ausgehenden Nachricht hinzu.
    
- So fügen Sie einem der Container im Adressbuch hinzu.
    
In beiden Szenarien wird ein Adressbuchanbieter aufgefordert, eine einmalige Tabelle zurückzugeben. Adressbuchanbieter können entweder eine einzelne einmalige Tabelle implementieren, die in beiden Situationen verwendet werden soll, oder eine eindeutige einmalige Tabelle für jede Situation. 
  
Wenn der Empfänger in eine ausgehende Nachricht eingeschlossen wird, ruft MAPI die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) des Adressbuchanbieters auf, um die einmalige Tabelle abzurufen. Die einmalige Tabelle enthält Vorlagen, mit denen ein Benutzer Informationen eingeben kann, die zur Erstellung eines Empfängers mit einer gültigen Adresse führen. MAPI registriert für Benachrichtigungen in dieser Tabelle und hält sie geöffnet, sodass Änderungen für den Benutzer widergespiegelt werden können. MAPI gibt die Tabelle nur frei, wenn die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Subsystem- oder Adressbuchstatusobjekts aufgerufen wird. 
  
Wenn der Empfänger einem Container hinzugefügt wird, führt MAPI einen anderen Aufruf durch und ruft die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, um seine **PR_CREATE_TEMPLATES** -Eigenschaft ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) abzurufen. Der in dieser einmaligen Tabelle enthaltene Vorlagensatz stellt die Empfängertypen dar, die dem Container hinzugefügt werden können. E-Mail-Server machen beispielsweise häufig einen Container für jedes installierte Gateway verfügbar, sodass jeder Container nur spezifische Adressen für das entsprechende Gateway enthält.
  
MAPI stellt eine einmalige Tabelle bereit, die eigene Vorlagen sowie Vorlagen von jedem Adressbuchanbieter in der Sitzung enthält. MAPI stellt eine generische Vorlage bereit, die zum Erstellen eines neuen Empfängers für jeden Adresstyp verwendet werden kann, vorausgesetzt, der Benutzer kennt das Format. Adressbuchanbieter verwenden diese einmalige Tabelle, indem [sie IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)aufrufen. Jede der Vorlagen, die in der MAPI-Einzeltabelle enthalten sind, führt zur Erstellung von Empfängern mit gültigen Empfängeradressen.
  
Adressbuchanbieter stellen in der Regel eine Vorlage für jeden unterstützten Adresstyp bereit. Die Unterstützung für Vorlagen ist jedoch nicht erforderlich. Adressbuchanbieter, die das Erstellen neuer Adressen nicht zulassen, können MAPI_E_NO_SUPPORT zurückgeben, wenn MAPI-Aufrufe eine einmalige Tabelle anfordern. Adressbuchanbieter, die die Erstellung neuer Adressen zulassen, aber keine Vorlagen bereitstellen, können **IMAPISupport::GetOneOffTable** aufrufen, um die in der EINMALIGEN MAPI-Tabelle aufgeführten Vorlagen zu verwenden. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in einmaligen Tabellen:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** gibt den Adresstyp an, der dem mit der Vorlage erstellten neuen Empfänger zugeordnet werden kann. 
  
 **PR_DISPLAY_NAME** und **PR_DISPLAY_TYPE** Daten dem neuen Empfänger zuordnen. **PR_DISPLAY_NAME** enthält eine Zeichenfolge, die den neuen Empfänger identifiziert, und **PR_DISPLAY_TYPE** eine Konstante enthält, die den Typ des Symbols angibt, das mit der Zeile angezeigt werden soll. Für Vorlagen für Messagingbenutzer ist **die PR_DISPLAY_TYPE** Spalte auf DT_MAILUSER festgelegt. Für Vorlagen für Verteilerlisten ist **die PR_DISPLAY_TYPE** Spalte auf DT_DISTLIST festgelegt. 
  
 **PR_ENTRYID** ist der Eintragsbezeichner der Vorlage, die zum Erstellen eines neuen Empfängers verwendet werden soll. Dieser Eintragsbezeichner kann an zukünftige [IAddrBook::NewEntry-,](iaddrbook-newentry.md) [IAddrBook::OpenEntry-](iaddrbook-openentry.md)und [IABContainer::CreateEntry-Aufrufe](iabcontainer-createentry.md) übergeben werden. Container legen die **PR_ENTRYID** Spalte ihrer Zeile für die Standardmäßige Messaging-Benutzervorlage auf **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und die **PR_ENTRYID** Spalte ihrer Zeile für die Standardverteilungslistenvorlage auf **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) fest. 
  
 **PR_DEPTH** wird verwendet, um die hierarchische Anzeige der Einträge in einer einmaligen Tabelle zu unterstützen, indem die Einzugsebene für die Vorlage angegeben wird. Obwohl einmalige Tabellen entweder als flache Liste oder als hierarchische Anzeige angezeigt werden können, ist letzteres vorzuziehen, und Adressbuchanbieter sollten dies unterstützen, indem sie die **PR_DEPTH** Spalte für jede Zeile entsprechend festlegen. **PR_DEPTH** nullbasiert ist; Zeilen mit dem Wert 0 in ihrer **PR_DEPTH** Spalte werden nicht eingezogen. Je höher der Wert von **PR_DEPTH** ist, desto mehr wird die Zeile eingezogen. Beispielsweise werden Zeilen mit **PR_DEPTH** auf 1 festgelegt, um eine Registerkarte eingezogen, während Zeilen mit **PR_DEPTH** auf 3 festgelegt sind, drei Registerkarten eingezogen sind. 
  
 **PR_SELECTABLE** wird verwendet, um anzugeben, ob eine Zeile in der Tabelle eine Vorlage darstellt, die ausgewählt und zum Erstellen eines neuen Empfängers verwendet werden kann. Obwohl die meisten Zeilen in einer einmaligen Tabelle Vorlagen darstellen, können Anbieter Zeilen enthalten, die keine Vorlagen sind. Beispielsweise kann ein Anbieter die einmalige Tabelle nach Vorlagentyp organisieren, einschließlich einer Kategoriezeile, die in der Anzeige angezeigt wird, aber nicht für die Empfängererstellung verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

