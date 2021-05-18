---
title: Abschnitte des MapiSvc.inf-Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405562"
---
# <a name="mapisvcinf-service-provider-sections"></a>Abschnitte des MapiSvc.inf-Dienstanbieters

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf enthält einen Dienstanbieterabschnitt für jeden der Einträge, die im Eintrag **Anbieter** im vorherigen Abschnitt "Nachrichtendienste" aufgeführt sind. **Dienstanbieterabschnitte** ähneln Nachrichtendienstabschnitten, da beide Arten von Abschnitten Einträge in diesem Format enthalten: 
  
**property-Tag** = Eigenschaftswert 
  
Dienstanbieterabschnitte und Nachrichtendienstabschnitte unterscheiden sich jedoch darin, dass solche Eigenschaftseinträge der einzige Eintragstyp sind, der in Dienstanbieterabschnitten enthalten ist. Es kann keine zusätzlichen oder verknüpften Abschnitte für Dienstanbieter sein. Alle Dienstanbieterinformationen müssen in dem einen Abschnitt enthalten sein. 
  
Einige der in Nachrichtendienstabschnitten festgelegten Eigenschaften werden auch in Abschnitten des Dienstanbieters festgelegt, da diese Eigenschaften für beides sinnvoll sind. Die **PR_DISPLAY_NAME-Eigenschaft** ist ein Beispiel. Sowohl Dienstanbieter als auch Nachrichtendienste haben einen Namen, der für die Anzeige auf der Benutzeroberfläche der Konfiguration verwendet wird. Je nach Dienstanbieter ist dieser Name möglicherweise identisch. Andere Eigenschaften sind spezifisch für Dienstanbieter. 
  
Typische Dienstanbieterabschnitte umfassen die folgenden Einträge, die alle erforderlich sind:
  
**PR_DISPLAY_NAME**  =   _string_
  
**PR_PROVIDER_DISPLAY**  =   _string_
  
**PR_PROVIDER_DLL_NAME**  =   _Name der DLL-Datei_
  
**PR_RESOURCE_TYPE**  =   _long_
  
**PR_RESOURCE_FLAGS**  =   _bitmask_
  
Der **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) ist ähnlich wie **PR_SERVICE_DLL_NAME**; Es gibt den Dateinamen für die DLL an, die den Dienstanbieter enthält. Nachrichtendienstcode kann bei einem seiner Dienstanbieter in derselben DLL-Datei gespeichert werden oder als separate DLL vorhanden sein. Beachten Sie, dass unabhängig von der Zielplattform kein Suffix im Eintrag enthalten ist. MAPI übernimmt bei Bedarf das Hinzufügen eines Suffixes. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) -Eintrag stellt den Typ des Dienstanbieters dar; Dienstanbieter legen sie auf die entsprechende vordefinierte Konstante fest. Gültige Werte sind MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER und MAPI_AB_PROVIDER.
  
Ein weiterer Eigenschaftseintrag, der sowohl für Nachrichtendienste als auch für Dienstanbieter gilt, **gibt PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) -Eintrag Optionen an. Die Einstellungen für diesen Eigenschaftseintrag können je nach Dienstanbieter variieren. Einige Nachrichtenspeicheranbieter können z. B. PR_RESOURCE_FLAGS auf STATUS_NO_DEFAULT_STORE festlegen, wenn sie niemals als Standardnachrichtenspeicher verwendet werden können.  
  
Es folgen drei Beispiele für Dienstanbieterabschnitte. Der **Abschnitt [Ab-Anbieter]** ist der Abschnitt Dienstanbieter für den Standard-Adressbuchdienst. Die **Abschnitte [MsgService Prov1]** und **[MsgService Prov2]** gehören zu My Own Service; Der erste Abschnitt ist ein Adressbuchanbieter, der zweite ein Abschnitt nachrichtenspeicheranbieter. 
  
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


