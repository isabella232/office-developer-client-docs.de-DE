---
title: Erforderliche Funktionen für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328693"
---
# <a name="required-features-for-address-book-providers"></a>Erforderliche Funktionen für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter können mit vorübergehenden oder permanenten, lokalen oder remote gespeicherten Empfängerinformationen arbeiten, die von einem oder mehreren Messagingsystemen verständlich sind und für eine Datenträgerdatei oder Datenbanktabelle formatiert sind. Es gibt eine Vielzahl von Features, die ein Adressbuchanbieter implementieren kann, wodurch der Wert erhöht und die Interoperabilität mit Clients und anderen Anbietern verbessert wird. Es sind jedoch einige Features erforderlich.
  
In der folgenden Tabelle werden die Features beschrieben, die von allen Adressbuch Anbietern benötigt werden, sowie die Schritte, die Sie ausführen müssen, um Sie zu implementieren.
  
|**Feature**|**VorGehensWeise**|
|:-----|:-----|
|Sitzungs Anmeldung  <br/> | Implementieren Sie eine Einstiegspunktfunktion. Weitere Informationen finden Sie unter [Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implementieren Sie die [IABProvider:: Login](iabprovider-logon.md) -Methode. Weitere Informationen finden Sie unter [Implementieren des Adressbuch Anbieters bei der Anmeldung und Abmeldung](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Sitzungsabmeldung  <br/> |Implementieren Sie die [IABProvider:: Shutdown](iabprovider-shutdown.md) -Methode. Weitere Informationen finden Sie unter [Implementieren des Adressbuch Anbieters bei der Anmeldung und Abmeldung](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Erstellen von Eintrags Bezeichnern  <br/> |Unterstützung für die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft. Weitere Informationen finden Sie unter [MAPI](mapi-entry-identifiers.md) -Eintrags-IDs und [Adressbuch Bezeichner](address-book-identifiers.md).  <br/> |
|Beitrag zur Statustabelle  <br/> | Implementieren Sie die entsprechenden Methoden der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle. Weitere Informationen finden Sie unter [Implementierung von Status Objekten](status-object-implementation.md).  <br/>  Unterstützen der erforderlichen Statustabellen Eigenschaften. Weitere Informationen finden Sie unter [Status Tabellen](status-tables.md).  <br/>  Rufen Sie [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md)auf.  <br/> |
|Unterstützung für eingeschränkte Statusobjekte  <br/> | Implementieren Sie die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode.  <br/>  Zurückgeben von MAPI_E_NO_SUPPORT von den anderen **IMAPIStatus** -Methoden.  <br/> |
|Unterstützung der interaktiven und programmgesteuerten Konfiguration  <br/> | Implementieren Sie eine Einstiegspunktfunktion für den Nachrichtendienst.  <br/>  Implementieren Sie eine Anzeigetabelle. Weitere Informationen finden Sie unter [Anzeige Tabellen](display-tables.md) und [Anzeige Tabellen Implementierung](display-table-implementation.md).  <br/>  Implementieren Sie ein Eigenschaftenfenster, oder rufen Sie die [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode auf. Weitere Informationen finden Sie unter [Eigenschaftenblatt Implementierung](property-sheet-implementation.md).  <br/> |
   
Wenn Ihr Anbieter die Empfänger Erstellung unterstützt, müssen Sie darüber hinaus eine Liste mit Erstellungsvorlagen angeben. Geben Sie diese Liste an, indem Sie die [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) -Methode implementieren, um alle Vorlagen einzuschließen, die von Ihrem Anbieter unterstützt werden, und die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode jedes Containers zum Öffnen des **PR_CREATE_TEMPLATES** ([ Pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft und enthält alle Vorlagen, die vom Container unterstützt werden. Weitere Informationen finden Sie unter [Implementieren von einmaligen Tabellen](implementing-one-off-tables.md).
  

