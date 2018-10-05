---
title: PidTagContainerFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389183"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske der Flags, die ein Adressbuchcontainer Funktionen beschreiben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Kennung:  <br/> |0x3600  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden:
  
AB_FIND_ON_OPEN 
  
> Zeigt ein Dialogfeld zum Anfordern einer Einschränkung vor dem Anzeigen der Inhalt des Containers an. 
    
AB_MODIFIABLE 
  
> Einträge können hinzugefügt und aus dem Container entfernt werden. Dieses Kennzeichen gibt nicht an, ob alle Einträge im Container geändert werden können.
    
AB_RECIPIENTS 
  
> Der Container kann Empfänger enthalten. Dieses Kennzeichen werden nicht angegeben, gibt an, ob alle Empfänger tatsächlich in den Container vorhanden sind, oder gibt an, ob sie hinzugefügt oder entfernt werden können. 
    
AB_SUBCONTAINERS 
  
> Der Container kann untergeordnete Container enthalten. Dieses Kennzeichen nicht an, ob alle Untercontainer tatsächlich in den Container vorhanden sind, noch, ob sie hinzugefügt oder entfernt werden können. AB_SUBCONTAINERS muss für den Container zur Unterstützung von [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)festgelegt werden. 
    
AB_UNMODIFIABLE 
  
> Einträge können nicht hinzugefügt oder aus dem Container entfernt werden. Dieses Kennzeichen gibt nicht an, ob alle Einträge im Container geändert werden können. 
    
Das Flag AB_FIND_ON_OPEN empfiehlt sich insbesondere für Container mit online-Dienste oder langsame Verbindung zum Server verwendet. Wenn ein Container, die AB_FIND_ON_OPEN festgelegt wurde geöffnet wird, wird ein Dialogfeld **Suchen** für den Benutzer zum Einschränken der angezeigten messaging Benutzer angezeigt. Sogar eine teilweise Spezifikation Einschränken der messaging-Benutzer kann eine Darstellung des Inhalts erheblich beschleunigen. 
  
Die AB_MODIFIABLE oder AB_UNMODIFIABLE-Flag muss festgelegt werden. Beide Flags können festgelegt werden, um anzugeben, dass es sich bei der Container nicht bekannt ist, ob sie oder nicht kann beispielsweise geändert werden, wenn der Benutzer Zugriffsrechte Änderung abhängt. In diesem Fall muss eine Clientanwendung versuchen, einen Anruf und untersuchen den Rückgabecode um das Container-Funktionen zu bestimmen. Ein Client gestartet wird normalerweise durch AB_MODIFIABLE untersuchen. Wenn sie festgelegt ist, wird der Client, die versucht, den Container geändert und überprüft den Rückgabewert aufgerufen. 
  
Die Kennzeichen AB_MODIFIABLE gibt die Einträge werden kann nicht zum Container hinzugefügt. Um dies zu bestimmen, sollte der Client die entsprechende [OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen des Containers **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft verwenden. Öffnende **PR_CREATE_TEMPLATES** Ursachen des Containers einmaligen Tabelle zurückgegeben werden soll, Auflisten der Arten von Einträgen, die im Container erstellt werden können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet ein Client-Kommunikation mit einem Server (NSPI = Name Service Provider Interface).
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

