---
title: Implementieren einer einmaligen Anbieter-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792546"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementieren einer einmaligen Anbieter-Tabelle

  
  
**Betrifft**: Outlook 
  
MAPI-Aufrufen des Anbieters [GetOneOffTable](iablogon-getoneofftable.md) -Methode auf, wenn der Benutzer von einer Clientanwendung eine ausgehende Nachricht einen Empfänger hinzufügt. In der Regel sind die angeforderte Adresstypen für Ihr messaging-System eindeutig. Wenn der Anbieter Empfänger erstellen unterstützt, muss sie eine einmalige Tabelle bereitstellen, die Vorlagen für jede Art von unterstützten Empfängeradresse verfügbar macht. Wird vom Dienstanbieter Recipient Creation nicht unterstützt, muss zurückgegeben Sie MAPI_E_NO_SUPPORT aus den Anruf **GetOneOffTable** . 
  
MAPI wird in der Regel geöffnetem einmaligen Tabelle des Anbieters für die Lebensdauer der Sitzung freigegeben wurde, nur, wenn ein Client des Subsystems aufruft oder Adresse des Buchs [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode. MAPI registriert für Benachrichtigungen in dieser Tabelle, sodass Vorlagen hinzugefügt oder gelöscht werden, diese Änderungen an den Benutzer widergespiegelt werden können. 
  
 **GetOneOffTable implementieren**
  
1. Überprüfen Sie den Wert des Flags-Parameters, _UlFlags_. Wenn die Option MAPI_UNICODE festgelegt ist und der Anbieter keine Unicode unterstützt, ein Fehler auftritt, und geben Sie MAPI_E_BAD_CHARWIDTH zurück. 
    
2. Überprüfen Sie, ob vom Dienstanbieter einmaligen Tabelle bereits erstellt worden ist. Da einmalige Tabellen in der Regel statisch sind, muss der Anbieter nie durch den Erstellungsvorgang nur einmal. Wenn bereits eine Tabelle vorhanden ist, wird zurückkehren Sie einen Zeiger zu ihm. 
    
3. Wenn eine einmalige Tabelle noch nicht vorhanden ist, rufen Sie **CreateTable** um eine zu erstellen. 
    
4. Legen Sie die folgenden Eigenschaften für die Spalten in der Tabellenzeilen:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) auf den Namen des Typs des Empfängers, die die Vorlage erstellen können. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) an die Eintrags-ID für die einmaligen Vorlage.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) an, dass der Hierarchieebene in der einmaligen Tabelle werden angezeigt.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) auf "true", um anzugeben, ob die Zeile einer Vorlage und FALSE darstellt.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), die der Art der Adresse, die von der Vorlage erstellt.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER oder einen anderen Wert, der die Art der Anzeige für die Vorlage angibt.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) in einen eindeutigen Binärwert. 
    
5. Rufen Sie [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) , um die Tabelle direkt zu ändern. 
    
6. Rufen Sie [ITableData::HrGetView](itabledata-hrgetview.md) So erstellen Sie eine **IMAPITable** Implementierung der Aufrufer zurückgegeben. 
    

