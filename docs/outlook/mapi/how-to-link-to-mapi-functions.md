---
title: Verweisen auf MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346883"
---
# <a name="link-to-mapi-functions"></a>Verweisen auf MAPI-Funktionen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei Methoden zum Verknüpfen: implizite Verknüpfung, explizite Verknüpfung und ein neues Hybridmodell mithilfe der MAPI-Stubbibliothek.
  
## <a name="implicit-linking"></a>Implizite Verknüpfung

In der Vergangenheit war beim Aufrufen von MAPI-Funktionen in einer Messaginganwendung immer die Verknüpfung mit der Mapi32.lib-Bibliothek erforderlich. Dazu gehörten Routing-MAPI-Aufrufe an die Windows-MAPI-Stubbibliothek Mapi32.dll, die die Aufrufe dann zur Laufzeit an die standardmäßige MAPI-Clientimplementierung weiterleitet. Dieser Aufrufprozess wird als implizite Verknüpfung bezeichnet. Die linke Seite der folgenden Abbildung zeigt ein Beispiel für implizite Verknüpfungen, die in einem Aufrufprozess für MAPI-Funktionen verwendet werden. Der Prozess wird von einer MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32.lib) und den Windows-MAPI-Stub (Mapi32.dll) und wird durch die Outlook-MAPI-Clientimplementierung des MAPI-Stubs (Msmapi32.dll) abgeschlossen.
  
**Vergleich der impliziten und expliziten Verknüpfung.**

![Vergleich der impliziten und expliziten Verknüpfung](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich der impliziten und expliziten Verknüpfung")
  
## <a name="explicit-linking"></a>Explizite Verknüpfung

Da der standardmäßige MAPI-Client die On-Demand-Installation mithilfe des Windows Installer (MSI) unterstützt, können Sie Messaginganwendungen direkt im Outlook-MAPI-Stub entwickeln, anstatt die MAPI-Bibliothek und den Windows zu verwenden. Die rechte Seite der vorherigen Abbildung zeigt ein Beispiel für einen AUFRUFprozess der MAPI-Funktion, beginnend mit einer MAPI-Anwendung, die nach dem Pfad und dem DLL-Namen für den Outlook-MAPI-Stub sucht (Schritt 2 im folgenden Abschnitt), und das Aufrufen von Funktionsaufrufen in den Outlook-MAPI-Stub (Schritt 3 im folgenden Abschnitt). Im folgenden Verfahren wird gezeigt, wie Sie MAPI-Funktionen mithilfe expliziter Verknüpfungen aufrufen. 
  
> [!NOTE]
> Diese Informationen zur expliziten Verknüpfung sind möglicherweise überflüssig für Ihre Anforderungen mit der Einführung der MAPIStubLibrary.lib, die im folgenden Abschnitt erläutert wird. Wie das implizite Modell verwaltet die neue Bibliothek alles und implementiert die explizite Verknüpfungslogik, die Outlook MAPI direkt lädt. 
  
Weitere Informationen zu expliziten Verknüpfungen finden Sie unter Linking Explicitly.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>So rufen Sie MAPI-API-Elemente ohne die MAPI-Bibliothek und den Windows-MAPI-Stub auf

1. Erstellen Sie in Ihrer Programmdatei eine globale Liste von Funktionszeigern für jedes von Ihnen verwendete MAPI-API-Element. 
    
   Das folgende Beispiel zeigt diesen Schritt.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Erstellen Sie eine Funktion, die MAPI-Funktionen initialisiert, um eine Verknüpfung mit der MAPI-DLL des standardmäßigen MAPI-Clients (z. B. Msmapi32.dll von Microsoft Outlook). Gehen Sie in dieser Funktion wie folgt vor: 
    
    1. Laden mapi32.dll aus dem entsprechenden Systemverzeichnis. 
        
       |||
       |:-----|:-----|
       |x64 oder x86 nativ  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 im WoW-Modus  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Rufen Sie [die FGetComponentPath-Funktion auf,](fgetcomponentpath.md) um den Pfad und den DLL-Namen zu erhalten, der das MAPI-Subsystem implementiert. Weitere Informationen finden Sie unter [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Laden Sie die DLL, indem Sie die LoadLibrary-Funktion aufrufen. 
        
    4. Initialisieren Sie das MAPI-Funktionszeigerarray, indem Sie die GetProcAddress-Funktion aufrufen. 
        
    Das folgende Beispiel zeigt die vorherigen Schritte:
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. Rufen Sie schließlich die Funktion auf, die Sie in Schritt 2 in Ihrer Messaginganwendung erstellt haben, bevor Sie Aufrufe von MAPI-API-Elementen starten. 
    
   > [!CAUTION]
   > Sie müssen die Initialisierung des MAPI-Subsystems vor dem Schließen der Anwendung uninitialisieren. 
  
   Das folgende Beispiel zeigt diesen Schritt: 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

Die Einführung Microsoft Outlook 2010 und 64-Bit-MAPI, die nun auf die Microsoft Outlook 2013 erweitert wird, erfordert mehr als die herkömmliche 32-Bit-API für die vollständige Implementierung. Ein neues Projekt, die MAPI-Stubbibliothek, das auf der CodePlex-Website veröffentlicht wird, bietet einen Drop-In-Ersatz für Mapi32.lib, das das Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt. MAPIStubLibrary.lib entfällt die Notwendigkeit, explizit mit MAPI zu verknüpfen, und nachdem Sie sie erstellt haben, können Sie Mapi32.lib aus Ihren Linkereinstellungen entfernen und durch MAPIStubLibrary.lib ersetzen. Es sollten keine weiteren Änderungen am Code erforderlich sein. Außerdem ist es nicht **erforderlich, LoadLibrary-,** **GetProcAddress-** und **FreeLibrary-Code** zu schreiben, um neuere Exporte zu verarbeiten, die in dieser Bibliotheksdatei enthalten sind, jedoch nicht in Mapi32.lib, was bei Verwendung expliziter Verknüpfungen erforderlich wäre. 
  
Einige der neuen Funktionen, die mit dieser Bibliothek verknüpft sind, die in Mapi32.lib nicht verfügbar sind, umfassen Folgendes:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Eine alternative Methode zum Integrieren der MAPI-Stubbibliothek besteht im Kopieren der Quelldateien MapiStubLibrary.cpp und StubUtils.cpp direkt in Ihr Projekt, und entfernen Sie alle Verknüpfungen mit Mapi32.lib und code, der explizit mit MAPI verknüpft ist.
  
Informationen zum Zugriff auf die MAPI-Stubbibliotheksdateien und Informationen zum Erstellen und Integrieren in Ihr Projekt sowie Fragen zu dieser Bibliothek, z. B. wann und warum sie verwendet werden sollen, finden Sie in der [MAPI-Stubbibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md)
- [Installieren von MAPI-Headerdateien](how-to-install-mapi-header-files.md)
- [Auswählen einer bestimmten Version der zu ladende MAPI](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Bestimmen der zu verwendenden Verknüpfungsmethode](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Verknüpfen einer ausführbaren Datei mit einer DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

