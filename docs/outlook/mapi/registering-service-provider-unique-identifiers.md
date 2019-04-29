---
title: Registrieren von eindeutigen Bezeichnern des Dienstanbieters
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
# <a name="registering-service-provider-unique-identifiers"></a>Registrieren von eindeutigen Bezeichnern des Dienstanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuch, Nachrichtenspeicher und Transportanbieter verwenden einen eindeutigen Bezeichner, der als [MAPIUID](mapiuid.md) bezeichnet wird, um Dienstobjekte unterschiedlicher Typen zu registrieren. Ein **MAPIUID** ist ein 16-Byte-Bezeichner, der eine GUID enthält. Mithilfe des folgenden Verfahrens können Sie eine **MAPIUID** erstellen: 
  
1. Definieren Sie eine Konstante.
    
2. Rufen Sie das Visual Studio*Create GUID** Tool auf. 
    
Ein Adressbuchanbieter kann beispielsweise die folgende Konstante in eine Headerdatei aufnehmen, um eine **MAPIUID**zu definieren:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **So registrieren Sie eine MAPIUID, wenn es sich bei Ihrem Anbieter um ein Adressbuch oder einen Nachrichtenspeicher Anbieter handelt**
  
1. Rufen Sie [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md)auf.
    
2. Registrieren Sie ein **MAPIUID** für jedes Anmeldeobjekt, das Sie instanziieren, und fügen Sie dieses **MAPIUID** in die ersten 16 Bytes des **ab** -Elements jeder Eintrags-ID ein, die Sie erstellen. MAPI verwendet **MAPIUID** -Strukturen zum Zuordnen von Objekten zu Dienstanbietern. Wenn ein Client die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, um ein Objekt zu öffnen, untersucht MAPI den **MAPIUID** -Teil des Eintrags Bezeichners, der mit dem registrierten **MAPIUID**übereinstimmt, um zu bestimmen, welches Anmeldeobjekt das öffnen soll. Anfrage.
    
3. Wenn es sich bei Ihrem Anbieter um einen Transport handelt, registrieren Sie eine oder mehrere **MAPIUID** -Strukturen, wenn MAPI Ihre **IXPLogon:: AddressTypes** -Methode aufruft. MAPI verwendet die von Transportanbietern registrierten **MAPIUID** -Strukturen, um die Zuständigkeit für die Nachrichtenübermittlung zuzuweisen. 
    
Obwohl Dienstanbieter in der Regel ein einzelnes **MAPIUID**registrieren, können Sie mehrere **MAPIUID** -Strukturen registrieren. Wenn Ihr Adressbuch oder der Nachrichtenspeicher Anbieter mehrere Anmeldeobjekte unterstützt, können Sie möglicherweise ein anderes **MAPIUID** für jedes Logon-Objekt implementieren, indem Sie einem Benutzer erlauben, mehrere Instanzen Ihres Anbieters zu Ihrem Profil hinzuzufügen. Es gibt einige weitere Gründe, mehr als eine **MAPIUID**zu unterstützen:
  
- Sie müssen mehr als eine Version Ihres Anbieters unterstützen, und die Eintrags-IDs müssen die entsprechende Version darstellen. Weisen Sie für jede Version einen anderen **MAPIUID** zu. 
    
- Sie möchten zwischen den von Ihnen unterstützten Objekttypen unterscheiden. Ein Adressbuchanbieter kann beispielsweise ein **MAPIUID** registrieren, um es in den Eintrags Bezeichnern seiner Messaging-Benutzerobjekte zu verwenden, und ein anderes **MAPIUID** für Verteilerlisten verwenden. 
    
Wenn mehrere Anmeldeobjekte gleichzeitig aktiv sind, ist es sinnvoll, für jeden eine eindeutige **MAPIUID** -Struktur zu besitzen. Dadurch wird die Genauigkeit erhöht, mit der MAPI Eingabe-IDs mit Dienstanbietern vergleicht und einige Arbeitsvorgänge spart. Wenn jedes Logon-Objekt seinen eigenen eindeutigen Bezeichner hat, kann MAPI sicherstellen, dass jede Anforderung, die an ein LOGON-Objekt weitergeleitet wird, von diesem Objekt verarbeitet werden kann. Wenn Anmeldeobjekte **MAPIUID** -Strukturen freigeben, leitet MAPI die Anforderung an das erste Anmeldeobjekt weiter, das von der **MAPIUID**identifiziert wird. Wenn eines Ihrer Anmeldeobjekte eine Anforderung erhält, dass es nicht verarbeitet werden kann, da es die Eintrags-ID nicht verarbeitet, leiten Sie die Anforderung an das nächste Anmeldeobjekt weiter, bevor Sie einen Fehler zurückgeben.
  
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieter Anmeldung](implementing-service-provider-logon.md)

