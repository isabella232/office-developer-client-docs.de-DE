---
title: Registrieren von Service Provider eindeutige Bezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795360"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrieren von Service Provider eindeutige Bezeichner

  
  
**Betrifft**: Outlook 
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen einen eindeutigen Bezeichner, der als ein [MAPIUID](mapiuid.md) bezeichnet, um auf Serviceobjekte der verschiedenen Typen registrieren. Ein **MAPIUID** ist ein 16-Byte-Bezeichner, der eine GUID enthält. Sie können eine **MAPIUID** mithilfe des folgenden Verfahrens erstellen: 
  
1. Definieren Sie eine Konstante.
    
2. Rufen Sie die Visual Studio-*GUID erstellen** Tool. 
    
Adressbuch-Dienstanbieter möglicherweise beispielsweise die folgenden Konstanten in einer Headerdatei zum Definieren einer **MAPIUID**enthalten:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Eine MAPIUID registriert, wenn der Anbieter einen Address Book oder einer Nachricht-Anbieter ist**
  
1. Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registrieren einer **MAPIUID** für die einzelnen Anmeldung Objekt zurück, das Sie instanziieren, und Schließen dieses **MAPIUID** in den ersten 16 Byte des Elements **Ab** der jedes Eintrags-ID, die Sie erstellen. MAPI verwendet **MAPIUID** Strukturen Dienstanbieter Objekte zugeordnet. Wenn ein Client aufruft, dass die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode zum Öffnen eines Objekts, MAPI den **MAPIUID** Teil des Bezeichners Eintrag untersucht, sollte anschließendem Abgleich mit der registrierten **MAPIUID**, zu bestimmen, welches Objekt Anmeldung öffnen erhalten Anforderung.
    
3. Wenn der Anbieter einen Transport ist, registrieren Sie ein oder mehrere **MAPIUID** Strukturen, wenn MAPI Ihrer **IXPLogon::AddressTypes** -Methode aufruft. MAPI verwendet die vom Transportanbieter für registriert **MAPIUID** Strukturen, die Verantwortung für die Nachrichtenübermittlung zuzuweisen. 
    
Obwohl-Dienstanbieter in der Regel ein einzelnes **MAPIUID**registrieren, können Sie mehrere **MAPIUID** Strukturen registrieren. Wenn Ihr Adressbuch oder die Nachricht vom Anbieter unterstützt mehrere Logon-Objekten, möglicherweise speichern Anwesenheitsebene einen Benutzer mehr als eine Instanz des Anbieters zu deren Profil hinzufügen, möchten Sie möglicherweise eine unterschiedliche **MAPIUID** für jedes Objekt Anmeldung zu implementieren. Es gibt einige andere Gründe zur Unterstützung von mehr als eine **MAPIUID**:
  
- Sie müssen mehr als eine Version des Anbieters unterstützen, und die Eintragsbezeichner müssen die entsprechende Version darstellen. Zuweisen einer anderen **MAPIUID** für jede Version. 
    
- Unterscheiden zwischen den Typen von Objekten, die Sie unterstützen möchten. Beispielsweise möchten ein Adressbuchanbieter Registrieren einer **MAPIUID** in der Eintragsbezeichner seiner messaging User-Objekte verwenden und eine unterschiedliche **MAPIUID** für Verteilerlisten verwenden. 
    
Wenn mehrere Logon-Objekten, die gleichzeitig aktiv sind vorhanden sind, ist es sinnvoll, die jeweils eindeutige **MAPIUID** -Strukturen haben. Dadurch wird die Genauigkeit, mit der MAPI entspricht-Eintragsbezeichner Dienstanbietern und erspart einige, erhöht. Bei jeder Anmeldung-Objekt eine eigene eindeutige ID besitzt, MAPI kann zu gewährleisten, dass alle anfordern Routen zu einem Anmeldeobjekt können durch dieses Objekt behandelt werden. Wenn Logon-Objekten **MAPIUID** Strukturen freigeben, leitet MAPI die Anforderung auf der ersten Anmeldung-Objekt, das durch die **MAPIUID**identifiziert wird. Wenn eine der Logon-Objekten eine Anforderung, die nicht verarbeitet werden kann empfängt, da die Eintrags-ID nicht bearbeitet werden kann, übergeben Sie die Anforderung an die nächste Anmeldung-Objekt vor der Rückgabe eines Fehlers.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Service Provider Anmeldung](implementing-service-provider-logon.md)

