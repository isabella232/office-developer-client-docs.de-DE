---
title: Auswählen einer bestimmten zu ladenden MAPI-Version
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344520"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Auswählen einer bestimmten zu ladenden MAPI-Version

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie eine explizite Verknüpfung mit einer MAPI-Implementierung herstellen, müssen Sie sorgfältig auswählen, welche Implementierung geladen werden soll. 
  
Es gibt zwei Methoden, um explizit eine Implementierung von MAPI zu verknüpfen. 
  
1. Sie können die MAPI-Stub-Bibliothek laden und in der Registrierung eine benutzerdefinierte DLL angeben, um MAPI-Aufrufe zu laden und zu senden.
    
2. Sie können den MAPI-clientlookup-Algorithmus implementieren, um die vom Standard-e-Mail-Client verwendete Version von MAPI zu suchen und zu laden.
    
Da Sie die [Mapi32. dll-Stub-Registrierungseinstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) so ändern können, dass Ihre Anwendung eine beliebige Implementierung von MAPI verwendet, empfehlen wir, dass Sie Ihre Anwendung zur Verwendung einer MAPI-Implementierung leiten, die Sie mit getestet haben. Im folgenden werden beide Methoden für die explizite Verknüpfung beschrieben. 
  
## <a name="reading-from-the-registry"></a>Lesen aus der Registrierung

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>So lesen Sie MAPI-Implementierungsinformationen aus der Registrierung

1. Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für einen e-Mail-Client `HKLM\Software\Clients\Mail` anzeigen, befinden sich unter dem Schlüssel des e-Mail-Clients. 
    
   In der folgenden Tabelle werden diese Schlüssel beschrieben:
    
   |**Taste**|**Beschreibung**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Eine Windows Installer PublishComponent Category ID (GUID), die die DLL identifiziert, die Simple MAPI-oder MAPI-Aufrufe exportiert. Ist dieser Wert festgelegt, hat dieser Schlüssel Vorrang vor dem **DllPath** -oder **DLLPathEx** -Schlüssel.  <br/> |
   |MSIApplicationLCID  <br/> |Gebietsschemabezeichner (LCID) für die Anwendung. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel aus `HKLM\Software` , und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unterhalb dieses Schlüssels, die Gebietsschemainformationen enthalten.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs für Microsoft Office. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel aus `HKLM\Software` , und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unterhalb dieses Schlüssels.  <br/> |
   
   Rufen Sie die Informationen aus diesen Schlüsseln ab.
    
2. Übergibt die Werte, die Sie aus dem vorherigen Schritt erhalten haben, an die [FGetComponentPath](fgetcomponentpath.md) -Funktion. **FGetComponentPath** ist eine Funktion, die von der MAPI-Stub-Bibliothek mapistub. dll exportiert wird. Es gibt den Pfad der benutzerdefinierten Version von MAPI zurück. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>So laden Sie die MAPI-Implementierung als Standard

1. Lesen Sie `HKLM\Software\Clients\Mail::(default)` den Registrierungswert. 
    
2. Nachschlagen der Informationen für den angegebenen Client wie oben beschrieben.
    
> [!NOTE]
> Beachten Sie, dass der Standard-e-Mail-Client möglicherweise Extended MAPI nicht implementiert. 
  
#### <a name="example"></a>Beispiel

Um MAPI wie von Outlook zu laden, suchen Sie die Registrierungsschlüssel unter `HKLM\Software\Clients\Mail\Microsoft Outlook` , und geben Sie Sie an **FGetComponentPath**. **FGetComponentPath** gibt den Pfad für die MAPI-Implementierung von Outlook zurück. 
  
Wenn die Schlüssel **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den Registrierungswert **DLLPathEx** . Wenn die Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad der MAPI-Implementierung des Clients an. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementieren des MAPI-clientLookup-Algorithmus

In der folgenden Tabelle sind die vier Funktionen von MFCMAPI aufgeführt, die zum Nachschlagen des Pfads für eine benutzerdefinierte Implementierung von MAPI verwendet werden:
  
|**Funktion**|**Beschreibung**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Ruft den MAPI-Bibliothekspfad ab.  <br/> |
| `GetMailKey` <br/> |Ruft den MAPI-e-Mail-Registrierungsschlüssel ab.  <br/> |
| `GetMapiMsiIds` <br/> |Ruft den Windows Installer-Bezeichner ab.  <br/> |
| `GetComponentPath` <br/> |Ruft den Komponentenpfad mithilfe von [FGetComponentPath](fgetcomponentpath.md)ab.  <br/> |
   
Da MFCMAPI die Standardimplementierung von MAPI standardmäßig lädt, wenn Sie eine andere MAPI-Implementierung verwenden möchten, müssen Sie Sie explizit dazu leiten. Dies wird mithilfe der Session\Load- **MAPI** -Routine ausgeführt. 
  
### <a name="how-these-functions-work"></a>FunktionsWeise dieser Funktionen

1. MFCMAPI- `GetMAPIPath`Aufrufe, übergeben von NULL für den Client Parameter, um die standardmäßige MAPI-Implementierung zu laden.
    
2.  `GetMAPIPath`Aufrufe `GetMapiMsiIds` zum Lesen der Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`Aufrufe `GetMailKey` zum Öffnen des Registrierungsschlüssels für den standardmäßigen e-Mail-Client. 
    
4.  `GetMapiMsiIds`verwendet das Registrierungshandle zurückgegeben `GetMailKey` , um Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**zu suchen.
    
5. Die Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**werden an `GetMAPIPath`zurückgegeben.  `GetMAPIPath`übergibt sie an `GetComponentPath`.
    
6.  `GetComponentPath`lädt die MAPI-Stub-Bibliothek Mapi32. dll aus dem Systemverzeichnis. 
    
7.  `GetComponentPath`Ruft dann die Adresse der **FGetComponentPath** -Funktion aus Mapi32. dll ab, wobei davon ausgegangen wird, dass Mapi32. dll **FGetComponentPath**exportiert.
    
8. Wenn das Abrufen der Adresse von **FGetComponentPath** aus Mapi32. dll fehl `GetComponentPath` schlägt, ruft die Adresse aus mapistub. dll ab. 
    
9.  `GetComponentPath`Ruft dann **FGetComponentPath**auf, um den Pfad der Standard Version von MAPI abzurufen.
    
10.  `GetMAPIPath`gibt dann diesen Pfad an den Aufrufer zurück, der dann MAPI lädt und explizit mit ihm verknüpft ist, wie unter [Link zu MAPI Functions](how-to-link-to-mapi-functions.md)beschrieben.
    
> [!NOTE] 
> - Zur Unterstützung lokalisierter Kopien von MAPI für englische und nicht-englische Gebiets `GetMAPIPath` Schemas liest die Werte für die **MSIApplicationLCID** und **MSIOfficeLCID** .  `GetMAPIPath`Ruft dann **FGetComponentPath**auf, wobei zunächst **MSIApplicationLCID** als **SzQualifier**und erneut **MSIOfficeLCID** als **szQualifier**angegeben wird. Weitere Informationen zu Registrierungsschlüsseln für e-Mail-Clients, die nicht-englische Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Wenn MFCMAPI keinen Pfad für MAPI verwendet `GetMAPIPath`, wird die MAPI-Stub-Bibliothek aus dem Systemverzeichnis geladen.
> - Der **MSMapiApps** -Registrierungswert, der unter [explizitES Zuordnen von MAPI-aufrufen zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) erläutert wird, gilt nur, wenn die MAPI-Stub-Bibliothek verwendet wird. Anwendungen, die eine bestimmte MAPI-Implementierung laden oder die Standardimplementierung laden, müssen den Registrierungsschlüssel **MSMapiApps** nicht festlegen. 
    
## <a name="see-also"></a>Siehe auch

- [FGetComponentPath](fgetcomponentpath.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Verweisen auf MAPI-Funktionen](how-to-link-to-mapi-functions.md)
- [Mapi32. dll-Stub-Registrierungseinstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Explizites Zuordnen von MAPI-aufrufen zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

