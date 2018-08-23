---
title: Dienstanbieterabschnitte in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586781"
---
# <a name="mapisvcinf-service-provider-sections"></a>Dienstanbieterabschnitte in MapiSvc.inf

**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPISVC.inf enthält einen Dienst Anbieterabschnitt für jeden der Einträge in der **Anbieter** -Eintrag im vorherigen Abschnitt der Nachricht Dienste aufgeführt. **Service** Provider Abschnitte ähneln Nachricht Service Abschnitte, dass beide Arten von Abschnitten Einträge in diesem Format enthalten: 
  
**Eigenschafts-Tag** = Wert-Eigenschaft 
  
Unterscheiden sich jedoch Service Provider Abschnitte und Nachricht Service Abschnitte, solche Eigenschafteneinträge die einzige Art des Eintrags im Service Provider Abschnitte enthalten sind. Es kann keine zusätzliche oder verknüpfte Abschnitte für Dienstanbieter vorhanden sein. alle Informationen muss in einem Abschnitt enthalten sein. 
  
Einige der Eigenschaften in Nachricht Service Abschnitten festgelegt werden auch in Service Provider Abschnitten festgelegt, da diese Eigenschaften für beide sinnvoll. Die **PR_DISPLAY_NAME** -Eigenschaft ist ein Beispiel. Dienstanbieter und Message-Dienste haben einen Namen, der für die Anzeige in der Benutzeroberfläche für die Konfiguration verwendet wird. Je nach den Dienstanbieter diesem Namen oder möglicherweise nicht identisch. Andere Eigenschaften sind spezifisch für den Dienstanbieter. 
  
Normalen Service Provider Abschnitte enthalten die folgenden Einträge, die alle erforderlich sind:
  
**PR_DISPLAY_NAME** =  _Zeichenfolge_
  
**PR_PROVIDER_DISPLAY** =  _Zeichenfolge_
  
**PR_PROVIDER_DLL_NAME** =  _Name der DLL-Datei_
  
**PR_RESOURCE_TYPE** =  _lang_
  
**PR_RESOURCE_FLAGS** =  _Bitmaske_
  
**PR_SERVICE_DLL_NAME**entspricht der Eintrag **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) ist. Es gibt den Dateinamen für die DLL, die den Dienstanbieter enthält. Message Authentication Servicecode mit einem der der Dienstanbieter in der gleichen DLL-Datei gespeichert werden kann oder als eine separate DLL vorhanden ist. Beachten Sie, dass kein Suffix in den Eintrag unabhängig von der Zielplattform enthalten ist. MAPI kümmert ein Suffix hinzufügen, falls erforderlich. 
  
**PR_RESOURCE_TYPE** Eintrag ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) stellt den Typ des Dienstanbieters dar. Dienstanbieter, die jedoch auf die entsprechende vordefinierte Konstante festlegen. Gültige Werte sind MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER und "MAPI_AB_PROVIDER"..
  
Eine andere Eigenschafteneintrag, der auf Message-Dienste und -Dienstanbieter angewendet wird, gibt die Optionen der Eintrag **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) an. Die Einstellungen für diesen Eintrag-Eigenschaft können je nach den Dienstanbieter unterscheiden. Beispielsweise können einige Anbieter Nachricht **PR_RESOURCE_FLAGS** auf STATUS_NO_DEFAULT_STORE festgelegt, wenn sie nie als Standard-Informationsspeicher ausgeführt werden können. 
  
Führen Sie die drei Beispiele für Service Provider Abschnitte. Im Abschnitt **[AB Provider]** ist für den Standard-Adressbuch-Dienst Bereich Service Provider. Die Abschnitte **[MsgService Prov1]** und **[MsgService Prov2]** gehören zu meine eigenen Dienst. der erste ist ein Adressbuch Anbieterabschnitt und die zweite ist eine Nachrichtenspeicher Anbieterabschnitt. 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


