---
title: Wählen Sie eine bestimmte Version von MAPI geladen werden
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399732"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Wählen Sie eine bestimmte Version von MAPI geladen werden

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim explizit auf eine Implementierung der MAPI zu verknüpfen, müssen Sie die Implementierung zum Laden sorgfältig auswählen. 
  
Es gibt zwei Methoden zum expliziten eine Implementierung von MAPI verknüpfen. 
  
1. Sie können die MAPI-Stub-Bibliothek zu laden, und geben in der Registrierung, die eine benutzerdefinierte DLL zum Laden und Versenden von MAPI-Aufrufe.
    
2. Sie können implementieren den MAPI-Client-Lookup-Algorithmus zum Nachschlagen von der Version von MAPI, die von der standardmäßige e-Mail-Client verwendet und Laden es.
    
Da die [Mapi32.dll Stub Registrierungseinstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) , um die Anwendung für jede Implementierung von MAPI zu leiten nicht geändert werden kann, wird empfohlen, Sie leiten die Anwendung eine Implementierung von MAPI verwendet, die Sie mit getestet haben. Im folgenden werden beide Methoden explizit verknüpfen beschrieben. 
  
## <a name="reading-from-the-registry"></a>Lesen aus der Registrierung

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>MAPI-Implementierungsinformationen aus der Registrierung lesen

1. Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für e-Mail-Client angeben, befinden sich unter dem `HKLM\Software\Clients\Mail` -Schlüssel des e-Mail-Client. 
    
   In der folgenden Tabelle werden diese Schlüssel beschrieben:
    
   |**Schlüssel**|**Beschreibung**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Ruft auf eine Windows Installer PublishComponent Kategorie-ID (GUID), die die DLL identifiziert, die simple MAPI-als auch die MAPI exportiert. Wenn dieser Schlüssel festlegen, Vorrang vor der **DLL-Pfad** oder **DLLPathEx** Schlüssel hat.  <br/> |
   |MSIApplicationLCID  <br/> |Gebietsschema-ID (LCID) für die Anwendung. Die erste Zeichenfolge Wert identifiziert einen Unterschlüssel aus `HKLM\Software` und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unter diesem Schlüssel, die Gebietsschemainformationen enthalten.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs für Microsoft Office. Die erste Zeichenfolge Wert identifiziert einen Unterschlüssel aus `HKLM\Software` und nachfolgende Zeichenfolgenwerte Registrierungswerte unter diesem Schlüssel zu identifizieren.  <br/> |
   
   Rufen Sie die Informationen aus dieser Schlüssel.
    
2. Übergeben Sie die Werte, die Sie an die Funktion [FGetComponentPath](fgetcomponentpath.md) aus dem vorherigen Schritt abgerufen. **FGetComponentPath** ist eine Funktion, die durch die MAPI-Stub-Bibliothek Mapistub.dll exportiert wird. Es gibt den Pfad der benutzerdefinierten MAPI-Version. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>Laden Sie die Implementierung der MAPI als Standard markiert

1. Lesen der `HKLM\Software\Clients\Mail::(default)` Registrierungswert. 
    
2. Die Informationen für den angegebenen Client Nachschlagen Sie wie oben beschrieben.
    
> [!NOTE]
> Beachten Sie, dass der Standard-Mailclient Extended MAPI nicht implementieren kann. 
  
#### <a name="example"></a>Beispiel

Um MAPI gemäß der Implementierung von Outlook zu laden, Nachschlagen der Registrierungsschlüssel unter `HKLM\Software\Clients\Mail\Microsoft Outlook` und an **FGetComponentPath**übergeben. **FGetComponentPath** gibt den Pfad für die Implementierung von Outlook MAPI-zurück. 
  
Wenn der Schlüssel **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den Registrierungswert **DLLPathEx** . Wenn der Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad der Client-Implementierung von MAPI. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementieren des MAPI-Client-Lookup-Algorithmus

Die folgende Tabelle enthält die vier Funktionen von MFCMAPI (engl.), die zum Nachschlagen von den Pfad für eine benutzerdefinierte Implementierung der MAPI verwendet werden:
  
|**Funktion**|**Beschreibung**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Ruft den Pfad der MAPI-Bibliothek.  <br/> |
| `GetMailKey` <br/> |Ruft den MAPI-Mail-Registrierungsschlüssel ab.  <br/> |
| `GetMapiMsiIds` <br/> |Ruft die Windows Installer-ID ab.  <br/> |
| `GetComponentPath` <br/> |Ruft den Komponentenpfad [FGetComponentPath](fgetcomponentpath.md)verwenden.  <br/> |
   
Da MFCMAPI (engl.) die standardmäßige Implementierung von MAPI standardmäßig geladen wird, wenn Sie eine andere Implementierung von MAPI verwenden möchten, müssen Sie dies explizit anweisen. Dies erfolgt mithilfe der **Session\Load MAPI** -Routine. 
  
### <a name="how-these-functions-work"></a>Wie funktionieren diese Funktionen

1. MFCMAPI (engl.) Anrufe `GetMAPIPath`, das Übergeben von NULL für den Clientparameter, um die standardmäßige MAPI-Implementierung zu laden.
    
2.  `GetMAPIPath`Anrufe `GetMapiMsiIds` zum Lesen der Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds`Anrufe `GetMailKey` auf den Registrierungsschlüssel für den Standard-Mail-Client zu öffnen. 
    
4.  `GetMapiMsiIds`verwendet das Registrierung Handle zurückgegebene `GetMailKey` zum Nachschlagen von Werten für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**.
    
5. Die Werte für **MSIComponentID**, **MSIApplicationLCID**und **MSIOfficeLCID**, kehren zum `GetMAPIPath`.  `GetMAPIPath`Anschließend übergibt sie an `GetComponentPath`.
    
6.  `GetComponentPath`Lädt die MAPI-Stub-Bibliothek Mapi32.dll, aus dem Verzeichnis des Systems. 
    
7.  `GetComponentPath`die Adresse der **FGetComponentPath** -Funktion von Mapi32.dll, vorausgesetzt, dass Mapi32.dll **FGetComponentPath**exportiert wird abgerufen.
    
8. Wenn die Adresse des **FGetComponentPath** von Mapi32.dll fehlschlägt, erste `GetComponentPath` die Adresse aus Mapistub.dll abgerufen. 
    
9.  `GetComponentPath`Ruft dann **FGetComponentPath**, um den Pfad des die Standardversion des MAPI.
    
10.  `GetMAPIPath`Klicken Sie dann gibt dieser Pfad an den Anrufer, die anschließend geladen MAPI und explizit darauf verknüpft, wie in [Verbindung zu MAPI-Funktionen](how-to-link-to-mapi-functions.md)beschrieben.
    
> [!NOTE] 
> - Zur Unterstützung von lokalisierter Kopien der MAPI für Englisch und nicht-englischen Gebietsschemas `GetMAPIPath` liest die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID** .  `GetMAPIPath`Ruft dann **FGetComponentPath**, zuerst **MSIApplicationLCID** als **SzQualifier**angeben und erneut **MSIOfficeLCID** als **SzQualifier**angeben. Weitere Informationen zu Registrierungsschlüsseln für e-Mail-Clients, die nicht-englischen Sprachen unterstützen, finden Sie unter [Einstellung der MSI-Schlüssel für Ihr MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Wenn keine MFCMAPI (engl.) einen Pfad für die Verwendung von MAPI empfängt `GetMAPIPath`, es lädt die MAPI-Stub-Bibliothek aus dem Verzeichnis des Systems.
> - Der **MSMapiApps** Registrierungswert in [Explizit Zuordnen von MAPI-Aufrufe zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) erläuterten gilt nur, wenn die MAPI-Stub-Bibliothek verwendet wird. Anwendungen, die eine bestimmte Implementierung der MAPI laden oder laden die standardmäßige Implementierung müssen nicht den **MSMapiApps** Registrierungsschlüssel festgelegt. 
    
## <a name="see-also"></a>Siehe auch

- [FGetComponentPath](fgetcomponentpath.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Verweisen auf MAPI-Funktionen](how-to-link-to-mapi-functions.md)
- [Mapi32.dll Stub Registrierungseinstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Einrichten der MSI-Keys für die MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Zuordnen von explizit MAPI-Aufrufe zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

