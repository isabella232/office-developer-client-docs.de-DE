---
title: Registrieren eindeutiger Bezeichner des Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410175"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrieren eindeutiger Bezeichner des Dienstanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter verwenden einen eindeutigen Bezeichner, der [als MAPIUID](mapiuid.md) bezeichnet wird, um sich bei Dienstobjekten verschiedener Typen zu registrieren. Eine **MAPIUID** ist eine 16-Byte-ID, die eine GUID enthält. Sie können eine **MAPIUID mithilfe** des folgenden Verfahrens erstellen: 
  
1. Definieren Sie eine Konstante.
    
2. Rufen Sie das Visual Studio *GUID** erstellen auf. 
    
Ein Adressbuchanbieter kann z. B. die folgende Konstante in einer Headerdatei enthalten, um eine **MAPIUID zu definieren:**
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **So registrieren Sie eine MAPIUID, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist**
  
1. Rufen [Sie IMAPISupport::SetProviderUID auf.](imapisupport-setprovideruid.md)
    
2. Registrieren Sie **eine MAPIUID** für jedes Anmeldeobjekt, das Sie instanziieren, und fügen Sie diese **MAPIUID** in die ersten 16 Byte des **ab-Mitglieds** jedes Eintragsbezeichners ein, den Sie erstellen. MAPI verwendet **MAPIUID-Strukturen,** um Objekte Dienstanbietern zuzuordnen. Wenn ein Client die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, um ein Objekt zu öffnen, untersucht MAPI den **MAPIUID-Teil** des Eintragsbezeichners und vergleicht ihn mit der registrierten **MAPIUID**, um zu bestimmen, welches Anmeldeobjekt die offene Anforderung empfangen soll.
    
3. Wenn Ihr Anbieter ein Transport ist, registrieren Sie mindestens eine **MAPIUID-Struktur,** wenn MAPI Ihre **IXPLogon::AddressTypes-Methode** aufruft. MAPI verwendet die von Transportanbietern registrierten **MAPIUID-Strukturen,** um die Verantwortung für die Nachrichtenzustellung zuzuordnen. 
    
Obwohl Dienstanbieter in der Regel eine einzelne **MAPIUID registrieren,** können Sie mehrere **MAPIUID-Strukturen** registrieren. Wenn Ihr Adressbuch- oder Nachrichtenspeicheranbieter mehrere Anmeldeobjekte unterstützt, z. B. indem ein Benutzer mehrere Instanzen Ihres Anbieters zu seinem Profil hinzufügen kann, sollten Sie für jedes Anmeldeobjekt eine andere **MAPIUID** implementieren. Es gibt einige andere Gründe für die Unterstützung von mehr als einem **MAPIUID:**
  
- Sie müssen mehr als eine Version Ihres Anbieters unterstützen, und die Eintragsbezeichner müssen die entsprechende Version darstellen. Weisen Sie für jede Version eine andere **MAPIUID** zu. 
    
- Sie möchten zwischen den unterstützten Objekttypen unterscheiden. Beispielsweise kann ein Adressbuchanbieter eine **MAPIUID** registrieren, die in den Eintragsbezeichnern seiner Messagingbenutzerobjekte verwendet werden soll, und eine andere **MAPIUID,** die für Verteilerlisten verwendet werden soll. 
    
Wenn mehrere Anmeldeobjekte gleichzeitig aktiv sind, ist es sinnvoll, für jedes Objekt eindeutige **MAPIUID-Strukturen** zu haben. Dadurch wird die Genauigkeit erhöht, mit der MAPI Eintragsbezeichnern zu Dienstanbietern entspricht, und es wird etwas Arbeit gespart. Wenn jedes Anmeldeobjekt über einen eigenen eindeutigen Bezeichner verfügt, kann MAPI garantieren, dass jede Anforderung, die es an ein Anmeldeobjekt weiter leitet, von diesem Objekt verarbeitet werden kann. Wenn Anmeldeobjekte **MAPIUID-Strukturen** gemeinsam verwenden, leitet MAPI die Anforderung an das erste Anmeldeobjekt weiter, das durch die **MAPIUID identifiziert wird.** Wenn eines der Anmeldeobjekte eine Anforderung empfängt, die nicht verarbeiten kann, da die Eintrags-ID nicht verwendet wird, übergeben Sie die Anforderung an das nächste Anmeldeobjekt, bevor sie einen Fehler zurücksennen.
  
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

