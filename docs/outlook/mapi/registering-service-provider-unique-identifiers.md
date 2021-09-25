---
title: Registrieren eindeutiger Bezeichner des Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afdf2c475bf39379f8fed9953cb2c76891c6fc69
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586838"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrieren eindeutiger Bezeichner des Dienstanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter verwenden einen eindeutigen Bezeichner, der als [MAPIUID](mapiuid.md) bezeichnet wird, um sich bei Dienstobjekten verschiedener Typen zu registrieren. Eine **MAPIUID** ist ein 16-Byte-Bezeichner, der eine GUID enthält. Mit dem folgenden Verfahren können Sie eine **MAPIUID** erstellen: 
  
1. Definieren Sie eine Konstante.
    
2. Rufen Sie das Tool Visual Studio *GUID** erstellen auf. 
    
Beispielsweise kann ein Adressbuchanbieter die folgende Konstante in eine Headerdatei einschließen, um eine **MAPIUID** zu definieren:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **So registrieren Sie eine MAPIUID, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist**
  
1. Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)auf.
    
2. Registrieren Sie eine **MAPIUID** für jedes Anmeldeobjekt, das Sie instanziieren, und schließen Sie diese **MAPIUID** in die ersten 16 Bytes des **Ab-Elements** jedes Eintragsbezeichners ein, den Sie erstellen. MAPI verwendet **MAPIUID-Strukturen,** um Objekte Dienstanbietern zuzuordnen. Wenn ein Client die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, um ein Objekt zu öffnen, überprüft MAPI den **MAPIUID-Teil** des Eintragsbezeichners, der mit der registrierten **MAPIUID** übereinstimmt, um zu bestimmen, welches Anmeldeobjekt die offene Anforderung empfangen soll.
    
3. Wenn Es sich bei Ihrem Anbieter um einen Transport handelt, registrieren Sie eine oder mehrere **MAPIUID-Strukturen,** wenn mapi Ihre **IXPLogon::AddressTypes-Methode aufruft.** Die MAPI verwendet die **MAPIUID-Strukturen,** die von Transportanbietern registriert wurden, um die Verantwortung für die Nachrichtenübermittlung zuzuweisen. 
    
Obwohl Dienstanbieter in der Regel eine einzelne **MAPIUID** registrieren, können Sie mehrere **MAPIUID-Strukturen** registrieren. Wenn Ihr Adressbuch- oder Nachrichtenspeicheranbieter mehrere Anmeldeobjekte unterstützt, z. B. indem Sie einem Benutzer erlauben, dem Profil mehr als eine Instanz Ihres Anbieters hinzuzufügen, sollten Sie für jedes Anmeldeobjekt eine andere **MAPIUID** implementieren. Es gibt einige andere Gründe, um mehr als eine **MAPIUID** zu unterstützen:
  
- Sie müssen mehr als eine Version Ihres Anbieters unterstützen, und die Eintragsbezeichner müssen die entsprechende Version darstellen. Weisen Sie für jede Version eine andere **MAPIUID** zu. 
    
- Sie möchten zwischen den unterstützten Objekttypen unterscheiden. Ein Adressbuchanbieter möchte beispielsweise eine **MAPIUID** registrieren, die in den Eintragsbezeichnern seiner Messagingbenutzerobjekte verwendet werden soll, und eine andere **MAPIUID,** die für Verteilerlisten verwendet werden soll. 
    
Wenn mehrere Gleichzeitig aktive Anmeldeobjekte vorhanden sind, ist es sinnvoll, eindeutige **MAPIUID-Strukturen** für jedes Objekt zu verwenden. Dadurch erhöht sich die Genauigkeit, mit der die MAPI Eintragsbezeichner an Dienstanbieter abgleicht, und spart Arbeit. Wenn jedes Anmeldeobjekt über einen eigenen eindeutigen Bezeichner verfügt, kann MAPI garantieren, dass jede Anforderung, die es an ein Anmeldeobjekt weitergibt, von diesem Objekt verarbeitet werden kann. Wenn Anmeldeobjekte **MAPIUID-Strukturen** gemeinsam verwenden, leitet MAPI die Anforderung an das erste Anmeldeobjekt weiter, das von **MAPIUID** identifiziert wird. Wenn eines Ihrer Anmeldeobjekte eine Anforderung empfängt, die nicht verarbeitet werden kann, da es den Eintragsbezeichner nicht verarbeitet, übergeben Sie die Anforderung an das nächste Anmeldeobjekt, bevor Sie einen Fehler zurückgeben.
  
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

