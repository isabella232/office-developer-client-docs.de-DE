---
title: Link zu MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400145"
---
# <a name="link-to-mapi-functions"></a>Link zu MAPI-Funktionen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei Methoden verknüpfen: implizite Verknüpfung, explizite Verknüpfung und die MAPI-Stub-Bibliothek mit neuen Hybridmodell bereitgestellt.
  
## <a name="implicit-linking"></a>Implizite Verknüpfung

In der Vergangenheit beteiligt Aufrufen von MAPI-Funktionen in einer e-Mail-Anwendung immer auf die Objektbibliothek Mapi32.lib verknüpfen. Diese enthalten, MAPI-Anrufe an die die Windows-MAPI-Stub-Bibliothek "Mapi32.dll", die die Anrufe an die Implementierung der standardmäßigen MAPI-Client zur Laufzeit dann weitergeleitet. Dieser Prozess der Anruf wird als implizite Verknüpfung bezeichnet. Links in der folgenden Abbildung zeigt ein Beispiel für implizite Verknüpfung in einem MAPI-Funktion Anruf Prozess verwendet. Der Prozess wird durch eine MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32.lib) und den Windows-MAPI-Stub (Mapi32.dll) und abgeschlossen ist, indem Sie die Outlook-MAPI-Client-Implementierung der MAPI-Stub (Msmapi32.dll).
  
**Vergleich von impliziter und expliziter links.**

![Vergleich von impliziter und expliziter links] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich von impliziter und expliziter links")
  
## <a name="explicit-linking"></a>Explizites verknüpfen

Da der Standard-MAPI-Client Installation bei Bedarf mithilfe von Windows Installer (MSI) unterstützt, können Sie direkt auf die Outlook-MAPI-Stub statt der MAPI-Bibliothek und Windows MAPI-Stub Messaginganwendungen entwickeln. Im rechten Teil der vorherigen Abbildung zeigt ein Beispiel für einen MAPI-Funktion Anruf-Prozess, beginnend mit einem MAPI-Anwendung für den Pfad und Namen der DLL-Datei für den Outlook-MAPI-Stub (Schritt 2 im folgenden Abschnitt) suchen und tätigen von Anrufen in der Outlook-MAPI-Stub (Funktion Schritt 3 im folgenden Abschnitt). Das folgende Verfahren zeigt, wie MAPI-Funktionen aufrufen, mithilfe von expliziten verknüpfen. 
  
> [!NOTE]
> Diese Informationen zum Verknüpfen von expliziten möglicherweise überflüssig auf Ihre Bedürfnisse mit der Einführung von der MAPIStubLibrary.lib im folgenden Abschnitt erläutert. Wie die implizite Modell der neue Bibliothek alles verwaltet und implementiert die explizite verknüpfende Logik, die von Outlook lädt MAPI direkt. 
  
Weitere Informationen zum expliziten Verknüpfen finden Sie unter explizit verknüpfen.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>MAPI-API-Elemente ohne die MAPI-Bibliothek und den Windows-MAPI-Stub aufrufen

1. Erstellen Sie in der Programmdatei eine globale Liste Funktionszeiger für die einzelnen MAPI-API-Elemente, die Sie verwenden. 
    
   Das folgende Beispiel zeigt diesen Schritt.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Erstellen Sie eine Funktion, die MAPI-Funktionen zum Verknüpfen der MAPI-DLL des Standard-MAPI-Client (beispielsweise Msmapi32.dll von Microsoft Outlook) initialisiert. Folgendermaßen Sie in dieser Funktion vor: 
    
    1. Laden Sie mapi32.dll aus dem entsprechenden Systemverzeichnis. 
        
       |||
       |:-----|:-----|
       |X64 oder X86 systemintern  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |X86 auf WoW-Modus  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Rufen Sie die [FGetComponentPath](fgetcomponentpath.md) -Funktion, wenn Sie den Pfad und Name-DLL, die MAPI-Subsystems implementiert erhalten möchten. Weitere Informationen finden Sie unter [Wählen Sie eine bestimmte Version von MAPI zu laden](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Laden der DLL-Datei durch Aufrufen der LoadLibrary-Funktion. 
        
    4. Initialisieren Sie das MAPI-Funktion Zeiger Array durch Aufrufen der GetProcAddress-Funktion. 
        
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

3. Rufen Sie anschließend die Funktion, die Sie in Schritt 2 in Ihrer messaging-Anwendung erstellten, bevor Sie MAPI-API-Elemente aufrufen. 
    
   > [!CAUTION]
   > Sie müssen die MAPI-Subsystems Aufhebung der Initialisierung der vor dem Schließen der Anwendung. 
  
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

Die Einführung von Microsoft Outlook 2010 und 64-Bit-MAPI, jetzt Erweitern der Microsoft Outlook 2013, erfordert mehr als die herkömmliche 32-Bit-API für eine vollständige Implementierung. Ein neues Projekt die MAPI-Stub-Bibliothek veröffentlicht, auf der CodePlex-Website enthält Technik Ersatz für Mapi32.lib, die Erstellung von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt. MAPIStubLibrary.lib entfällt die Notwendigkeit zum expliziten MAPI verknüpfen und erstellt es, können Sie Mapi32.lib aus entfernen Einstelllungen Linker durch MAPIStubLibrary.lib ersetzen; keine weiteren Änderungen an Ihrem Code sollte erforderlich sein. Er überflüssig auch das Schreiben **LoadLibrary**und **GetProcAddress** **FreeLibrary** Code zum Behandeln von neuere Exporte enthalten in dieser Bibliotheksdatei jedoch nicht im Mapi32.lib, die erforderlich wäre, wenn Sie explizite Verknüpfung verwendet. 
  
Einige der neuen Funktionen aus dieser Bibliothek verknüpft, die in Mapi32.lib nicht verfügbar sind die folgenden:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Einbinden der MAPI-Stub-Bibliothek eine alternative Methode ist die Quelldateien, MapiStubLibrary.cpp und StubUtils.cpp, direkt in Ihr Projekt kopieren und entfernen jegliche Verknüpfung zu Mapi32.lib und Code, der explizit MAPI verknüpft.
  
MAPI-Stub-Bibliothek Computerdateien und Informationen zum Erstellen und integrieren sie in Ihrem Projekt als auch Fragen zu dieser Bibliothek wie wann und warum verwenden, finden Sie unter der [MAPI-Stub-Bibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md)
- [Installieren der MAPI-Headerdateien](how-to-install-mapi-header-files.md)
- [Auswählen einer bestimmten zu ladenden MAPI-Version](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Bestimmen der zu verwendenden verknüpfen Methode](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Verknüpfen einer ausführbaren Datei mit einer DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Einrichten der MSI-Keys für die MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

