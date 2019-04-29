---
title: Abschnitte des MapiSvc. inf-Dienstanbieters
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
# <a name="mapisvcinf-service-provider-sections"></a>Abschnitte des MapiSvc. inf-Dienstanbieters

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPISVC. inf enthält einen Abschnitt des Dienstanbieters für jeden Eintrag, der im Abschnitt **Anbieter** im vorherigen Nachrichtendienst aufgeführt ist. **Dienst** Anbieter Abschnitte ähneln den Nachrichtendienst Abschnitten darin, dass beide Typen von Abschnitten Einträge in diesem Format enthalten: 
  
**Property Tag** = Eigenschaftswert 
  
Dienstanbieter Abschnitte und Nachrichtendienst Abschnitte unterscheiden sich jedoch darin, dass es sich bei diesen Eigenschaften Einträgen um den einzigen Eintrags handelt, der in Dienstanbieter Abschnitten enthalten ist. Es kann keine zusätzlichen oder verknüpften Abschnitte für Dienstanbieter geben; Alle Dienstanbieterinformationen müssen im ersten Abschnitt enthalten sein. 
  
Einige der Eigenschaften, die in Nachrichtendienst Abschnitten festgelegt sind, werden auch in Dienstanbieter Abschnitten festgelegt, da diese Eigenschaften für beides sinnvoll sind. Die **PR_DISPLAY_NAME** -Eigenschaft ist ein Beispiel. Sowohl Dienstanbieter als auch Nachrichtendienste haben einen Namen, der für die Anzeige in der Konfigurations-Benutzeroberfläche verwendet wird. Je nach Dienstanbieter kann dieser Name nicht identisch sein. Andere Eigenschaften sind für Dienstanbieter spezifisch. 
  
Typische Dienstanbieter Abschnitte enthalten die folgenden Einträge, die alle erforderlich sind:
  
**PR_DISPLAY_NAME** =  -_Zeichenfolge_
  
**PR_PROVIDER_DISPLAY** =  -_Zeichenfolge_
  
**PR_PROVIDER_DLL_NAME** =  _Name der DLL-Datei_
  
**PR_RESOURCE_TYPE** =  _lang_
  
**PR_RESOURCE_FLAGS** =  __ -Bitmaske
  
Der **PR_PROVIDER_DLL_NAME** -Eintrag ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)) ähnelt **PR_SERVICE_DLL_NAME**; Es gibt den Dateinamen für die DLL an, die den Dienstanbieter enthält. Der Nachrichtendienst Code kann mit einem seiner Dienstanbieter in derselben DLL-Datei gespeichert werden oder als separate DLL vorhanden sein. Beachten Sie, dass in dem Eintrag kein Suffix enthalten ist, unabhängig von der Zielplattform; MAPI sorgt dafür, dass bei Bedarf ein Suffix hinzugefügt wird. 
  
**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))-Eintrag stellt den Typ des Dienstanbieters dar. Dienstanbieter legen Sie die entsprechende vordefinierte Konstante fest. Gültige Werte sind MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER und MAPI_AB_PROVIDER.
  
Ein anderer Eigenschafteneintrag, der sowohl für Nachrichtendienste als auch für Dienstanbieter gilt, gibt der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eintrag Optionen an. Die Einstellungen für diesen Eigenschafteneintrag können je nach Dienstanbieter unterschiedlich sein. Einige Nachrichtenspeicher Anbieter können **PR_RESOURCE_FLAGS** beispielsweise auf STATUS_NO_DEFAULT_STORE festlegen, wenn Sie niemals als Standardnachrichtenspeicher fungieren dürfen. 
  
Es folgen drei Beispiele für Dienstanbieter Abschnitte. Der Abschnitt **[ab Provider]** ist der Abschnitt Dienstanbieter für den standardMäßigen Adressbuchdienst. Die Abschnitte **[MsgService Prov1]** und **[MsgService Prov2]** gehören zu meinem eigenen Dienst; bei dem ersten handelt es sich um einen Adressbuchanbieter-Abschnitt, und der zweite ist ein Abschnitt für Nachrichtenspeicher Anbieter. 
  
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


