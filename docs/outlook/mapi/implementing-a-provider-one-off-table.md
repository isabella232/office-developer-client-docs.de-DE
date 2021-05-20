---
title: Implementieren eines Anbieters One-Off Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436293"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementieren eines Anbieters One-Off Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI ruft die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) Ihres Anbieters auf, wenn der Benutzer einer Clientanwendung einer ausgehenden Nachricht einen Empfänger hinzufügt. In der Regel sind die angeforderten Adresstypen für Ihr Messagingsystem eindeutig. Wenn Ihr Anbieter die Erstellung von Empfängern unterstützt, muss er eine einzelne Tabelle angeben, in der Vorlagen für jeden Typ unterstützter Empfängeradressen verfügbar gemacht werden. Wenn Ihr Anbieter die Erstellung von Empfängern nicht unterstützt, geben MAPI_E_NO_SUPPORT vom **GetOneOffTable-Aufruf** zurück. 
  
MAPI hält in der Regel die einmal geöffnete Tabelle Ihres Anbieters für die Lebensdauer der Sitzung offen und gibt sie nur frei, wenn ein Client die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Subsystems oder adressbuchs aufruft. MAPI registriert sich für Benachrichtigungen in dieser Tabelle, sodass beim Hinzufügen oder Löschen von Vorlagen diese Änderungen für den Benutzer widerspiegelt werden können. 
  
 **So implementieren Sie IABLogon::GetOneOffTable**
  
1. Überprüfen Sie den Wert des Flags-Parameters  _ulFlags_. Wenn das MAPI_UNICODE festgelegt ist und Ihr Anbieter Unicode nicht unterstützt, führen Sie einen Fehler aus, und geben Sie MAPI_E_BAD_CHARWIDTH. 
    
2. Überprüfen Sie, ob die einmal erstellte Tabelle Ihres Anbieters bereits erstellt wurde. Da die Tabellen in der Regel statisch sind, muss Ihr Anbieter den Erstellungsprozess niemals mehr als einmal durchgehen. Wenn bereits eine Tabelle vorhanden ist, geben Sie einen Zeiger auf sie zurück. 
    
3. Wenn noch keine einzige Tabelle vorhanden ist, rufen Sie **CreateTable auf,** um eine zu erstellen. 
    
4. Legen Sie die folgenden Eigenschaften für die Spalten in den Tabellenzeilen ein:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) auf den Namen des Empfängertyps, den die Vorlage erstellen kann. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) zur Eintrags-ID für die einmal vorlage.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) zum Angeben der Hierarchieebene in der Tabellenanzeige.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) auf TRUE, um anzugeben, ob die Zeile eine Vorlage und andernfalls FALSE darstellt.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) auf den Von der Vorlage erstellten Adresstyp an.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) auf DT_MAILUSER oder einen anderen Wert, der den Anzeigetyp für die Vorlage angibt.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) auf einen eindeutigen binären Wert. 
    
5. Rufen [Sie ITableData::HrModifyRow auf,](itabledata-hrmodifyrow.md) um die Tabelle direkt zu ändern. 
    
6. Rufen [Sie ITableData::HrGetView auf,](itabledata-hrgetview.md) um eine **IMAPITable-Schnittstellenimplementierung** zu erstellen, um zum Aufrufer zurückzukehren. 
    

