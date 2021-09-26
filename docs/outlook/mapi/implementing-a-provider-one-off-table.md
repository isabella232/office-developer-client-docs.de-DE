---
title: Implementieren einer Anbieter-One-Off-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 060f69c28484b8fe3a805af22ebe631c746425de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620786"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementieren einer Anbieter-One-Off-Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI ruft die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) Ihres Anbieters auf, wenn der Benutzer einer Clientanwendung einer ausgehenden Nachricht einen Empfänger hinzufügt. In der Regel sind die angeforderten Adressentypen für Ihr Messagingsystem eindeutig. Wenn Ihr Anbieter die Erstellung von Empfängern unterstützt, muss er eine einmalige Tabelle bereitstellen, die Vorlagen für jeden Typ unterstützter Empfängeradresse verfügbar macht. Wenn Ihr Anbieter die Empfängererstellung nicht unterstützt, geben Sie MAPI_E_NO_SUPPORT aus dem **GetOneOffTable-Aufruf** zurück. 
  
Die MAPI hält in der Regel die einmalige Tabelle Ihres Anbieters für die Lebensdauer der Sitzung geöffnet und gibt sie nur frei, wenn ein Client die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Subsystems oder des Adressbuchs aufruft. MAPI registriert sich für Benachrichtigungen in dieser Tabelle, sodass diese Änderungen für den Benutzer widergespiegelt werden können, wenn Vorlagen hinzugefügt oder gelöscht werden. 
  
 **So implementieren Sie IABLogon::GetOneOffTable**
  
1. Überprüfen Sie den Wert des Flags-Parameters _ulFlags._ Wenn das flag MAPI_UNICODE festgelegt ist und Ihr Anbieter Unicode nicht unterstützt, schlagen Sie fehl und geben MAPI_E_BAD_CHARWIDTH zurück. 
    
2. Überprüfen Sie, ob die einmalige Tabelle Ihres Anbieters bereits erstellt wurde. Da einmalige Tabellen in der Regel statisch sind, muss Ihr Anbieter den Erstellungsprozess nie mehrmals durchlaufen. Wenn bereits eine Tabelle vorhanden ist, geben Sie einen Zeiger darauf zurück. 
    
3. Wenn noch keine einmalige Tabelle vorhanden ist, rufen **Sie CreateTable** auf, um eine tabelle zu erstellen. 
    
4. Legen Sie die folgenden Eigenschaften für die Spalten in Den Tabellenzeilen fest:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zum Namen des Empfängertyps, den die Vorlage erstellen kann. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) zum Eintragsbezeichner für die einmalige Vorlage.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) an, um die Hierarchieebene in der Einmaligen Tabellenanzeige anzugeben.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) auf TRUE zurück, um anzugeben, ob die Zeile eine Vorlage darstellt, andernfalls FALSE.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) an den Von der Vorlage erstellten Adresstyp an.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) auf DT_MAILUSER oder einen anderen Wert, der den Typ der Anzeige für die Vorlage angibt.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) zu einem eindeutigen binären Wert. 
    
5. Rufen Sie [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) auf, um die Tabelle direkt zu ändern. 
    
6. Rufen Sie [ITableData::HrGetView](itabledata-hrgetview.md) auf, um eine **IMAPITable-Schnittstellenimplementierungen** zu erstellen, die an den Aufrufer zurückgegeben werden. 
    

