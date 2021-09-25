---
title: Auswählen einer bestimmten zu ladenden MAPI-Version
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b410d53dee76a7f812f270d5f81f15bc691431ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580132"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>Auswählen einer bestimmten zu ladenden MAPI-Version

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim expliziten Verknüpfen mit einer MapI-Implementierung müssen Sie sorgfältig auswählen, welche Implementierung geladen werden soll. 
  
Es gibt zwei Methoden, die explizit mit einer Implementierung der MAPI verknüpft werden können. 
  
1. Sie können die MAPI-Stubbibliothek laden und in der Registrierung eine benutzerdefinierte DLL angeben, an die MAPI-Aufrufe geladen und verteilt werden sollen.
    
2. Sie können den MAPI-Client-Suchalgorithmus implementieren, um die vom Standard-E-Mail-Client verwendete MAPI-Version nachzuschlagen und zu laden.
    
Da Sie die [Mapi32.dll Stub Registry-Einstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) so ändern können, dass Ihre Anwendung eine beliebige Implementierung der MAPI verwendet, wird empfohlen, dass Sie Ihre Anwendung an weisen, eine Implementierung der MAPI zu verwenden, mit der Sie getestet haben. Im Folgenden werden beide Methoden der expliziten Verknüpfung beschrieben. 
  
## <a name="reading-from-the-registry"></a>Lesen aus der Registrierung

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>So lesen Sie MAPI-Implementierungsinformationen aus der Registrierung

1. Die Registrierungsschlüssel, die eine benutzerdefinierte DLL für einen E-Mail-Client angeben, befinden sich unter dem  `HKLM\Software\Clients\Mail` Schlüssel des E-Mail-Clients. 
    
   In der folgenden Tabelle werden diese Schlüssel beschrieben:
    
   |**Taste**|**Beschreibung**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Eine Windows PublishComponent-Kategorie-ID (GUID) des Installationsprogramms, die die DLL identifiziert, die einfache MAPI- oder MAPI-Aufrufe exportiert. Wenn festgelegt, hat dieser Schlüssel Vorrang vor dem **DLLPath-** oder **DLLPathEx-Schlüssel.**  <br/> |
   |MSIApplicationLCID  <br/> |Gebietsschemabezeichner (Locale Identifier, LCID) für Ihre Anwendung. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel aus  `HKLM\Software` und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unter diesem Schlüssel, die Gebietsschemainformationen enthalten.  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs für Microsoft Office. Der erste Zeichenfolgenwert identifiziert einen Unterschlüssel von  `HKLM\Software` und nachfolgende Zeichenfolgenwerte identifizieren Registrierungswerte unter diesem Schlüssel.  <br/> |
   
   Rufen Sie die Informationen aus diesen Schlüsseln ab.
    
2. Übergeben Sie die Werte, die Sie aus dem vorherigen Schritt abgerufen haben, an die [FGetComponentPath-Funktion.](fgetcomponentpath.md) **FGetComponentPath** ist eine Funktion, die von der MAPI-Stubbibliothek Mapistub.dll exportiert wird. Es gibt den Pfad der benutzerdefinierten Version der MAPI zurück. 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>So laden Sie die Implementierung der als Standard markierten MAPI

1. Lesen Sie den  `HKLM\Software\Clients\Mail::(default)` Registrierungswert. 
    
2. Suchen Sie die Informationen für den angegebenen Client, wie zuvor beschrieben.
    
> [!NOTE]
> Beachten Sie, dass der Standard-E-Mail-Client möglicherweise keine erweiterte MAPI implementiert. 
  
#### <a name="example"></a>Beispiel

Um die MAPI wie von Outlook implementiert zu laden, suchen Sie nach den Registrierungsschlüsseln unter `HKLM\Software\Clients\Mail\Microsoft Outlook` und übergeben sie an **FGetComponentPath**. **FGetComponentPath** gibt den Pfad für die MapI-Implementierung Outlook zurück. 
  
Wenn die Schlüssel **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID** nicht festgelegt sind, überprüfen Sie den **DLLPathEx-Registrierungswert.** Wenn die Schlüssel festgelegt sind, gibt **FGetComponentPath** den Pfad der Clientimplementierung der MAPI an. 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>Implementieren des MAPI-Client-Nachschlagealgorithmus

In der folgenden Tabelle sind die vier Funktionen von MFCMAPI aufgeführt, die verwendet werden, um den Pfad für eine benutzerdefinierte Implementierung der MAPI nachzuschlagen:
  
|**Funktion**|**Beschreibung**|
|:-----|:-----|
| `GetMAPIPath` <br/> |Ruft den MAPI-Bibliothekspfad ab.  <br/> |
| `GetMailKey` <br/> |Ruft den MAPI-E-Mail-Registrierungsschlüssel ab.  <br/> |
| `GetMapiMsiIds` <br/> |Ruft die Windows Installer-ID ab.  <br/> |
| `GetComponentPath` <br/> |Ruft den Komponentenpfad mithilfe von [FGetComponentPath](fgetcomponentpath.md)ab.  <br/> |
   
Da MFCMAPI standardmäßig die Standardimplementierungen der MAPI lädt, müssen Sie sie explizit dazu anzuweisen, wenn Sie eine andere Implementierung der MAPI verwenden möchten. Dies erfolgt mithilfe der **Session\Load MAPI-Routine.** 
  
### <a name="how-these-functions-work"></a>Funktionsweise dieser Funktionen

1. MFCMAPI-Aufrufe  `GetMAPIPath` , die NULL für den Clientparameter übergeben, um die standardmäßige MAPI-Implementierung zu laden.
    
2.  `GetMAPIPath` Ruft  `GetMapiMsiIds` auf, um die Werte für **MSIComponentID**, **MSIApplicationLCID** und **MSIOfficeLCID** zu lesen.
    
3.  `GetMapiMsiIds` Aufrufe  `GetMailKey` zum Öffnen des Registrierungsschlüssels für den Standard-E-Mail-Client. 
    
4.  `GetMapiMsiIds` verwendet das von zurückgegebene Registrierungshandle,  `GetMailKey` um Nachschlagewerte für **MSIComponentID,** **MSIApplicationLCID** und **MSIOfficeLCID** zu suchen.
    
5. Die Werte für **MSIComponentID**, **MSIApplicationLCID** und **MSIOfficeLCID** werden an  `GetMAPIPath` zurückgegeben.  `GetMAPIPath` übergibt sie dann an  `GetComponentPath` .
    
6.  `GetComponentPath` lädt die MAPI-Stubbibliothek Mapi32.dll aus dem Systemverzeichnis. 
    
7.  `GetComponentPath` ruft dann die Adresse der **FGetComponentPath-Funktion** aus Mapi32.dll ab, wobei davon ausgegangen wird, dass Mapi32.dll **FGetComponentPath** exportiert.
    
8. Wenn beim Abrufen der Adresse von **FGetComponentPath** von Mapi32.dll ein Fehler auftritt,  `GetComponentPath` wird die Adresse aus Mapistub.dll abgerufen. 
    
9.  `GetComponentPath` ruft dann **FGetComponentPath auf** und ruft den Pfad der Standardversion der MAPI ab.
    
10.  `GetMAPIPath` gibt dann diesen Pfad an den Aufrufer zurück, der dann die MAPI lädt und explizit mit ihr verknüpft, wie unter [Link to MAPI Functions](how-to-link-to-mapi-functions.md)beschrieben.
    
> [!NOTE] 
> - Um lokalisierte Kopien der MAPI für englische und nicht englische Gebietsschemas zu unterstützen, `GetMAPIPath` lesen Sie die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID.**  `GetMAPIPath` ruft dann **FGetComponentPath auf,** wobei zuerst **MSIApplicationLCID** als **szQualifier** und erneut **MSIOfficeLCID** als **szQualifier** angegeben wird. Weitere Informationen zu Registrierungsschlüsseln für E-Mail-Clients, die nicht englischsprachige Sprachen unterstützen, finden Sie unter [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).   
> - Wenn MFCMAPI keinen Pfad für die MAPI-Verwendung  `GetMAPIPath` empfängt, wird die MAPI-Stubbibliothek aus dem Systemverzeichnis geladen.
> - Der unter ["Explizite Zuordnung von MAPI-Aufrufen zu MAPI-DLLs"](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) erläuterte **MSMapiApps-Registrierungswert** gilt nur, wenn die MAPI-Stub-Bibliothek verwendet wird. Anwendungen, die eine bestimmte Implementierung der MAPI laden oder die Standardimplementierungen laden, müssen den **Registrierungsschlüssel "MSMapiApps"** nicht festlegen. 
    
## <a name="see-also"></a>Siehe auch

- [FGetComponentPath](fgetcomponentpath.md)
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Verweisen auf MAPI-Funktionen](how-to-link-to-mapi-functions.md)
- [Mapi32.dll Stub Registry Einstellungen](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [Explizites Zuordnen von MAPI-Aufrufen zu MAPI-DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

