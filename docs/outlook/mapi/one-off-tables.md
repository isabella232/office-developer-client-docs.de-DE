---
title: Einmalige Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439527"
---
# <a name="one-off-tables"></a>Einmalige Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine einmalige Tabelle enthält Informationen zu den Vorlagen, die ein Adressbuchanbieter zum Erstellen neuer Empfänger unterstützt. Einmalige Tabellen werden von Adressbuch Anbietern, einzelnen Adressbuch Containern und von MAPI implementiert und können dauerhaft oder temporär sein. 
  
> [!NOTE]
> Verwechseln Sie die Vorlagen nicht in einmaligen Tabellen mit Vorlagen Bezeichnern; während ihre Zwecke ähnlich sind, sind Ihre Code Konstrukte nichts gleich. Vorlagen werden zum Erstellen von Empfängern eines bestimmten Typs verwendet, während Vorlagenbezeichner verwendet werden, um die Daten eines Empfängers zu binden, die zu einem Hostanbieter gehören, mit Code zur Unterstützung eines anderen Empfängers, die zu einem fremden Anbieter gehören. 
  
Clients erstellen neue Empfänger:
  
- Zum Hinzufügen zur Empfängerliste einer ausgehenden Nachricht.
    
- , Um einen der Container im Adressbuch hinzuzufügen.
    
In beiden Szenarien wird ein Adressbuchanbieter aufgefordert, eine einmalige Tabelle zurückzugeben. Adressbuchanbieter können entweder eine einzelne einmalige Tabelle implementieren, die in beiden Situationen verwendet werden soll, oder eine einmalige Tabelle für jede Situation. 
  
Wenn der Empfänger mit einer ausgehenden Nachricht eingeschlossen wird, ruft MAPI die [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) -Methode des Adressbuch Anbieters auf, um die einmalige Tabelle abzurufen. Die einmalige Tabelle enthält Vorlagen, mit denen ein Benutzerinformationen eingeben kann, die zur Erstellung eines Empfängers mit einer gültigen Adresse führen. MAPI registriert Benachrichtigungen in dieser Tabelle, sodass Änderungen für den Benutzer wiedergegeben werden können. MAPI gibt die Tabelle nur dann frei, wenn die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode des Subsystems oder des Adressbuchs aufgerufen wird. 
  
Wenn der Empfänger einem Container hinzugefügt wird, führt MAPI einen anderen Aufruf aus, der die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers zum Abrufen seiner **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft aufruft. Die in dieser einmaligen Tabelle enthaltenen Vorlagen stellen die Empfängertypen dar, die dem Container hinzugefügt werden können. E-Mail-Server setzen beispielsweise oft einen Container für jedes installierte Gateway aus, sodass jeder Container nur Adressen enthält, die für das entsprechende Gateway spezifisch sind.
  
MAPI bietet eine einmalige Tabelle, die eigene Vorlagen sowie Vorlagen von jedem Adressbuchanbieter in der Sitzung enthält. MAPI bietet eine generische Vorlage, die zum Erstellen eines neuen Empfängers für einen beliebigen Adresstyp verwendet werden kann, vorausgesetzt, der Benutzer weiß sein Format. Adressbuchanbieter verwenden diese einmalige Tabelle, indem Sie [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md)aufrufen. Jede der in der MAPI-einmaligen Tabelle enthaltenen Vorlagen resultiert in der Erstellung von Empfängern mit gültigen Empfängeradressen.
  
Adressbuchanbieter geben in der Regel eine Vorlage für jeden unterstützten Adresstyp an. Die Unterstützung von Vorlagen ist jedoch nicht erforderlich. Adressbuchanbieter, die das Erstellen neuer Adressen nicht zulassen, können MAPI_E_NO_SUPPORT zurückgeben, wenn MAPI-Aufrufe eine einmalige Tabelle anfordern. Adressbuchanbieter, die neue Adresserstellung zulassen, jedoch keine Vorlagen angeben, können **IMAPISupport:: GetOneOffTable** aufrufen, um die in der MAPI-einmaligen Tabelle aufgeführten Vorlagen zu verwenden. 
  
Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in einmaligen Tabellen:
  
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([Pidtagselectable (](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** gibt den Adresstyp an, der dem neuen Empfänger zugeordnet werden kann, der mit der Vorlage erstellt wurde. 
  
 **PR_DISPLAY_NAME** und **PR_DISPLAY_TYPE** ordnen Daten dem neuen Empfänger zu. **PR_DISPLAY_NAME** enthält eine Zeichenfolge, die den neuen Empfänger identifiziert, und **PR_DISPLAY_TYPE** enthält eine Konstante, die den Typ des Symbols angibt, das mit der Zeile angezeigt werden soll. Vorlagen für Messagingbenutzer haben Ihre **PR_DISPLAY_TYPE** -Spalte auf DT_MAILUSER festgelegt. Vorlagen für Verteilerlisten haben Ihre **PR_DISPLAY_TYPE** -Spalte auf DT_DISTLIST festgelegt. 
  
 **PR_ENTRYID** ist der Eintragsbezeichner der Vorlage, die zum Erstellen eines neuen Empfängers verwendet werden soll. Dieser Eintragsbezeichner kann an Future [IAddrBook::](iaddrbook-newentry.md)upentry, [IAddrBook:: OpenEntry](iaddrbook-openentry.md)und [IABContainer::](iabcontainer-createentry.md) CreateEntry-Aufrufe übergeben werden. Container legen Sie die **PR_ENTRYID** -Spalte ihrer Zeile für die standardmäßige Messaging-Benutzervorlage auf **PR_DEF_CREATE_MAILUSER** ([pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md)) und die **PR_ENTRYID** -Spalte ihrer Zeile für die Standardverteilerliste fest. Vorlage zu **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** wird verwendet, um die hierarchische Anzeige der Einträge in einer einmaligen Tabelle zu unterstützen, indem die Einzugsebene für die Vorlage angegeben wird. Obwohl einmalige Tabellen entweder als flache Liste oder als hierarchische Anzeige angezeigt werden können, ist Letztere vorzuziehen, und Adressbuchanbieter sollten Sie unterstützen, indem Sie die **PR_DEPTH** -Spalte für jede Zeile entsprechend festlegen. **PR_DEPTH** ist nullbasiert; Zeilen mit dem Wert 0 in Ihrer **PR_DEPTH** -Spalte werden nicht eingerückt. Je höher der Wert von **PR_DEPTH**ist, desto mehr wird die Zeile eingerückt. Beispielsweise sind Zeilen mit **PR_DEPTH** auf 1 eingerückt, während Zeilen mit **PR_DEPTH** auf 3 eingezogen werden. 
  
 **PR_SELECTABLE** wird verwendet, um anzugeben, ob eine Zeile in der Tabelle eine Vorlage darstellt, die ausgewählt und zum Erstellen eines neuen Empfängers verwendet werden kann. Obwohl die meisten Zeilen in einer einmaligen Tabelle Vorlagen darstellen, können Anbieter nicht Vorlagen Zeilen einbeziehen. Beispielsweise kann ein Anbieter die einmalige Tabelle nach Vorlagentyp organisieren, einschließlich einer Kategorie-Zeile, die in der Anzeige angezeigt wird, aber nicht für die Erstellung von Empfängern verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

