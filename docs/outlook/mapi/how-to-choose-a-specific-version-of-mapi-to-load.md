---
title: Auswählen einer bestimmten zu ladenden MAPI-Version
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344520"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Auswählen einer bestimmten zu ladenden MAPI-Version

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie explizit mit einer Implementierung von MAPI verknüpfen, müssen Sie sorgfältig auswählen, welche Implementierung geladen werden soll. 
  
Es gibt zwei Methoden, um explizit mit einer Implementierung von MAPI zu verknüpfen. 
  
1. Sie können die MAPI-Stubbibliothek laden und in der Registrierung eine benutzerdefinierte DLL zum Laden und Versenden von MAPI-Aufrufen angeben.
    
2. Sie können den MAPI-Client-Suchalgorithmus implementieren, um die vom Standard-E-Mail-Client verwendete Version von MAPI nach zu suchen und zu laden.
    
Da Sie die [Mapi32.dll-Stubregistrierungs-Einstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) ändern können, um Ihre Anwendung auf die Verwendung einer beliebigen Implementierung von MAPI zu verfeinern, empfehlen wir, dass Sie Ihre Anwendung zur Verwendung einer Implementierung von MAPI anfeinen, mit der Sie getestet haben. Im Folgenden werden beide Methoden der expliziten Verknüpfung beschrieben. 
  
## <a name="reading-from-the-registry"></a>Lesen aus der Registrierung

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>So lesen Sie MAPI-Implementierungsinformationen aus der Registrierung

1. Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für einen E-Mail-Client angeben, befinden sich unter dem  `HKLM\Software\Clients\Mail` Schlüssel des E-Mail-Clients. 
    
   In der folgenden Tabelle werden diese Schlüssel beschrieben:
    
   |**Taste**|**Beschreibung**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Eine Windows Installer PublishComponent Category ID (GUID), die die DLL identifiziert, die einfache MAPI- oder MAPI-Aufrufe exportiert. Wenn festgelegt, hat dieser Schlüssel Vorrang vor dem **DLLPath-** oder **DLLPathEx-Schlüssel.**  <br/> |
   |MSIApplicationLCID  <br/> |Locale Identifier (LCID) für Ihre Anwendung. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel aus und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unterhalb dieses Schlüssels, die  `HKLM\Software` Locale-Informationen enthalten.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs für Microsoft Office. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel aus und nachfolgende Zeichenfolgenwerte  `HKLM\Software` identifizieren Registrierungswerte unterhalb dieses Schlüssels.  <br/> |
   
   Rufen Sie die Informationen aus diesen Schlüsseln ab.
    
2. Übergeben Sie die Werte, die Sie aus dem vorherigen Schritt erhalten haben, an die [FGetComponentPath-Funktion.](fgetcomponentpath.md) **FGetComponentPath** ist eine Funktion, die von der MAPI-Stubbibliothek exportiert Mapistub.dll. Es gibt den Pfad der benutzerdefinierten Version von MAPI zurück. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>So laden Sie die Als Standard gekennzeichnete Implementierung von MAPI

1. Lesen Sie den  `HKLM\Software\Clients\Mail::(default)` Registrierungswert. 
    
2. Suchen Sie die Informationen für den angegebenen Client, wie zuvor beschrieben.
    
> [!NOTE]
> Beachten Sie, dass der Standard-E-Mail-Client möglicherweise keine erweiterte MAPI implementiert. 
  
#### <a name="example"></a>Beispiel

Um MAPI wie von der Outlook zu laden, suchen Sie die Registrierungsschlüssel unter, und übergeben Sie sie `HKLM\Software\Clients\Mail\Microsoft Outlook` an **FGetComponentPath**. **FGetComponentPath** gibt den Pfad für Outlook Implementierung von MAPI zurück. 
  
Wenn die Schlüssel **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den **DLLPathEx-Registrierungswert.** Wenn die Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad der Clientimplementierung von MAPI an. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementieren des MAPI-Client-Nachschlagealgorithmus

In der folgenden Tabelle sind die vier Funktionen aus MFCMAPI aufgeführt, die zum Suchen des Pfads für eine benutzerdefinierte Implementierung von MAPI verwendet werden:
  
|**Funktion**|**Beschreibung**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Ruft den PFAD der MAPI-Bibliothek ab.  <br/> |
| `GetMailKey` <br/> |Ruft den MAPI-E-Mail-Registrierungsschlüssel ab.  <br/> |
| `GetMapiMsiIds` <br/> |Ruft die Windows Installer-ID ab.  <br/> |
| `GetComponentPath` <br/> |Ruft den Komponentenpfad mithilfe von [FGetComponentPath ab.](fgetcomponentpath.md)  <br/> |
   
Da MFCMAPI standardmäßig die Standardimplementierung von MAPI lädt, müssen Sie dies explizit angeben, wenn Sie eine andere Implementierung von MAPI verwenden möchten. Dies erfolgt mithilfe der **Session\Load MAPI-Routine.** 
  
### <a name="how-these-functions-work"></a>Funktionsweise dieser Funktionen

1. MFCMAPI ruft  `GetMAPIPath` null für den Clientparameter ab, um die standardmäßige MAPI-Implementierung zu laden.
    
2.  `GetMAPIPath` Aufrufe  `GetMapiMsiIds` zum Lesen der Werte für **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID**.
    
3.  `GetMapiMsiIds` Aufrufe  `GetMailKey` zum Öffnen des Registrierungsschlüssels für den Standard-E-Mail-Client. 
    
4.  `GetMapiMsiIds` verwendet das von zurückgegebene Registrierungshandle zum Suchen nach Werten  `GetMailKey` für **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID**.
    
5. Die Werte für **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID** werden an  `GetMAPIPath` zurückgegeben.  `GetMAPIPath` und übergibt sie dann an  `GetComponentPath` .
    
6.  `GetComponentPath` lädt die MAPI-Stubbibliothek Mapi32.dll aus dem Systemverzeichnis. 
    
7.  `GetComponentPath`ruft dann die Adresse der **FGetComponentPath-Funktion** aus Mapi32.dll ab, wenn Mapi32.dll **FGetComponentPath exportiert.**
    
8. Wenn das Abrufen der **Adresse von FGetComponentPath** aus Mapi32.dll, ruft die Adresse  `GetComponentPath` aus dem Mapistub.dll. 
    
9.  `GetComponentPath` ruft dann **FGetComponentPath auf,** um den Pfad der Standardversion von MAPI zu erhalten.
    
10.  `GetMAPIPath`gibt dann diesen Pfad an den Aufrufer zurück, der dann MAPI lädt und explizit darauf verknüpft, wie unter [Link zu MAPI-Funktionen beschrieben.](how-to-link-to-mapi-functions.md)
    
> [!NOTE] 
> - Um lokalisierte Kopien von MAPI für englische und nicht englische Locales zu unterstützen, werden die Werte für die Unterschlüssel  `GetMAPIPath` **MSIApplicationLCID** und **MSIOfficeLCID** gelesen.  `GetMAPIPath` ruft dann **FGetComponentPath auf,** gibt zuerst **MSIApplicationLCID** als **szQualifier** an und erneut **MSIOfficeLCID** als **szQualifier** an. Weitere Informationen zu Registrierungsschlüsseln für E-Mail-Clients, die nicht englische Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Wenn MFCMAPI keinen Pfad für MAPI mit erhält, wird die  `GetMAPIPath` MAPI-Stubbibliothek aus dem Systemverzeichnis geladen.
> - Der in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) erläuterte **MSMapiApps-Registrierungswert** gilt nur, wenn die MAPI-Stubbibliothek verwendet wird. Anwendungen, die eine bestimmte Implementierung von MAPI laden oder die Standardimplementierung laden, müssen den **Registrierungsschlüssel MSMapiApps** nicht festlegen. 
    
## <a name="see-also"></a>Siehe auch

- [FGetComponentPath](fgetcomponentpath.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Verweisen auf MAPI-Funktionen](how-to-link-to-mapi-functions.md)
- [Mapi32.dll stub Registry Einstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Explizites Zuordnen von MAPI-Aufrufen zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

