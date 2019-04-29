---
title: Implementieren einer einmaligen Anbieter Tabelle
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
# <a name="implementing-a-provider-one-off-table"></a>Implementieren einer einmaligen Anbieter Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI Ruft die [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) -Methode Ihres Anbieters auf, wenn der Benutzer einer Clientanwendung einer ausgehenden Nachricht einen Empfänger hinzufügt. In der Regel sind die angeforderten Adresstypen für Ihr Messagingsystem eindeutig. Wenn Ihr Anbieter die Empfänger Erstellung unterstützt, muss er eine einmalige Tabelle bereitstellen, die Vorlagen für alle unterstützten Empfängeradressen verfügbar macht. Wenn Ihr Anbieter die Empfänger Erstellung nicht unterstützt, geben Sie MAPI_E_NO_SUPPORT aus dem **GetOneOffTable** -Aufruf zurück. 
  
In der Regel wird die einmalige Tabelle Ihres Anbieters für die gesamte Lebensdauer der Sitzung geöffnet, und Sie wird nur dann freigegeben, wenn ein Client die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode des Subsystems oder des Adressbuchs aufruft. MAPI registriert für Benachrichtigungen in dieser Tabelle, sodass diese Änderungen für den Benutzer reflektiert werden können, wenn Vorlagen hinzugefügt oder gelöscht werden. 
  
 **So implementieren Sie IABLogon:: GetOneOffTable**
  
1. Überprüfen Sie den Wert des flags-Parameters _ulFlags_. Wenn das MAPI_UNICODE-Flag festgelegt ist und Ihr Anbieter Unicode nicht unterstützt, schlagen Sie fehl und geben MAPI_E_BAD_CHARWIDTH zurück. 
    
2. Überprüfen Sie, ob die einmalige Tabelle Ihres Anbieters bereits erstellt wurde. Da einmalige Tabellen in der Regel statisch sind, muss Ihr Anbieter den Erstellungsprozess nie mehr als einmal durchlaufen. Wenn bereits eine Tabelle vorhanden ist, geben Sie einen Zeiger darauf zurück. 
    
3. Wenn noch keine einmalige Tabelle vorhanden ist, rufen Sie **Create** Table auf, um eine zu erstellen. 
    
4. Legen Sie die folgenden Eigenschaften für die Spalten in den Tabellenzeilen fest:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) an den Namen des Empfängertyps, der von der Vorlage erstellt werden kann. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) an die Eintrags-ID für die einmalige Vorlage.
    
  - **PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md)), um die Hierarchieebene in der einmaligen Tabellenanzeige anzugeben.
    
  - **PR_SELECTABLE** ([Pidtagselectable (](pidtagselectable-canonical-property.md)) auf true, um anzugeben, ob die Zeile eine Vorlage darstellt, andernfalls false.
    
  - **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) an den Typ der von der Vorlage erstellten Adresse.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) an DT_MAILUSER oder einen anderen Wert, der den Anzeigetyp für die Vorlage angibt.
    
  - **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md)) an einen eindeutigen Binärwert. 
    
5. Rufen Sie [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) auf, um die Tabelle direkt zu ändern. 
    
6. Rufen Sie [ITableData:: HrGetView](itabledata-hrgetview.md) auf, um eine **IMAPITable** -Schnittstellenimplementierung zum zurückkehren zum Aufrufer zu erstellen. 
    

