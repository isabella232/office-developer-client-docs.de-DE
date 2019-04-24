---
title: Verweisen auf MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346883"
---
# <a name="link-to-mapi-functions"></a>Verweisen auf MAPI-Funktionen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt drei Methoden der Verknüpfung: implizite Verknüpfung, explizite Verknüpfung und ein neues Hybridmodell mithilfe der MAPI-Stub-Bibliothek.
  
## <a name="implicit-linking"></a>Implizite Verknüpfung

Historisch gesehen war das Aufrufen von MAPI-Funktionen in einer Messaginganwendung immer mit der Verknüpfung zur Mapi32. lib-Bibliothek verbunden. Hierzu gehörten das Weiterleiten von MAPI-Aufrufen an die Windows-MAPI-Stub-Bibliothek Mapi32. dll, die die Aufrufe dann zur Laufzeit an die standardmäßige MAPI-Client-implementierte. Dieser Anruf Prozess wird als implizite Verknüpfung bezeichnet. Die linke Seite der folgenden Abbildung zeigt ein Beispiel für eine implizite Verknüpfung, die in einem MAPI-Funktionsaufruf Prozess verwendet wird. Der Prozess wird von einer MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32. lib) und den Windows-MAPI-Stub (Mapi32. dll) und wird durch die Outlook-MAPI-Clientimplementierung des MAPI-Stub (msmapi32. dll) abgeschlossen.
  
**Vergleich der impliziten und expliziten Verknüpfung.**

![Vergleich der impliziten und expliziten Verknüpfung] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich der impliziten und expliziten Verknüpfung")
  
## <a name="explicit-linking"></a>Explizite Verknüpfung

Da der standardmäßige MAPI-Client die on-Demand-Installation mithilfe von Windows Installer (MSI) unterstützt, können Sie Messaginganwendungen direkt im Outlook-MAPI-Stub erstellen, anstatt die MAPI-Bibliothek und Windows MAPI-Stub zu verwenden. Die Rechte Seite der vorherigen Abbildung zeigt ein Beispiel für einen MAPI-Funktionsaufruf Prozess, beginnend mit einer MAPI-Anwendung, die nach dem Pfad und dem DLL-Namen für den Outlook-MAPI-Stub sucht (Schritt 2 im folgenden Abschnitt) und Funktionsaufrufe in den Outlook-MAPI-Stub ( Schritt 3 im folgenden Abschnitt). Im folgenden Verfahren wird gezeigt, wie Sie MAPI-Funktionen mithilfe der expliziten Verknüpfung aufrufen. 
  
> [!NOTE]
> Diese Informationen über die explizite Verknüpfung können auf Ihre Anforderungen mit der Einführung der MAPIStubLibrary. lib überflüssig werden, die im folgenden Abschnitt erläutert wird. Wie beim impliziten Modell verwaltet die neue Bibliothek alles und implementiert die explizite Verknüpfungslogik, die Outlooks MAPI direkt lädt. 
  
Weitere Informationen zur expliziten Verknüpfung finden Sie unter Verknüpfen explizit.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>So rufen Sie MAPI-API-Elemente ohne MAPI-Bibliothek und Windows MAPI-Stub auf

1. Erstellen Sie in Ihrer Programmdatei eine globale Liste der Funktionszeiger für jedes MAPI-API-Element, das Sie verwenden. 
    
   Das folgende Beispiel zeigt diesen Schritt.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Erstellen Sie eine Funktion, die MAPI-Funktionen für die Verknüpfung mit der MAPI-DLL des Standard-MAPI-Clients (beispielsweise msmapi32. dll von Microsoft Outlook) initialisiert. Führen Sie in dieser Funktion folgende Aktionen aus: 
    
    1. Laden Sie Mapi32. dll aus dem entsprechenden Systemverzeichnis. 
        
       |||
       |:-----|:-----|
       |x64 oder x86 nativ  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 im WoW-Modus  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Rufen Sie die [FGetComponentPath](fgetcomponentpath.md) -Funktion auf, um den Pfad und den DLL-Namen abzurufen, der das MAPI-Subsystem implementiert. Weitere Informationen finden Sie unter [Auswählen einer bestimmten zu ladenDEN MAPI-Version](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Laden Sie die DLL, indem Sie die LoadLibrary-Funktion aufrufen. 
        
    4. Initialisieren Sie das MAPI-Funktionszeiger Array, indem Sie die GetProcAddress-Funktion aufrufen. 
        
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

3. Rufen Sie schließlich die in Schritt 2 erstellte Funktion in der Messaginganwendung auf, bevor Sie Aufrufe an MAPI-API-Elemente durchführen. 
    
   > [!CAUTION]
   > Sie müssen das MAPI-Subsystem vor dem Schließen der Anwendung aufteilen. 
  
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary. lib

Die Einführung von Microsoft Outlook 2010 und 64-Bit MAPI, die sich jetzt auf Microsoft Outlook 2013 erstreckt, erfordert mehr als die herkömmliche 32-Bit-API für die vollständige Implementierung. Ein neues Projekt, die MAPI-Stub-Bibliothek, die auf der CodePlex-Website veröffentlicht wurde, bietet einen Ersatz für Mapi32. lib, der das Erstellen von 32-Bit-und 64-Bit-MAPI-Anwendungen unterstützt. MAPIStubLibrary. lib beseitigt die Notwendigkeit der expliziten Verknüpfung zu MAPI, und nachdem Sie erstellt wurde, können Sie Mapi32. lib aus ihren Linker-Einstellungen entfernen, indem Sie Sie durch MAPIStubLibrary. lib ersetzen. Es sollten keine weiteren Änderungen am Code erforderlich sein. Außerdem ist es nicht mehr erforderlich, **LoadLibrary**-, **GetProcAddress**-und **FreeLibrary** -Code zu schreiben, um neuere Exporte in diese Bibliotheksdatei zu verarbeiten, jedoch nicht in Mapi32. lib, die erforderlich wäre, wenn Sie eine explizite Verknüpfung verwenden würden. 
  
Zu den neuen Funktionen, die von dieser Bibliothek verknüpft sind und in Mapi32. lib nicht verfügbar sind, gehören die folgenden:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Eine alternative Methode zum Integrieren der MAPI-Stub-Bibliothek besteht darin, die Quelldateien MapiStubLibrary. cpp und StubUtils. cpp direkt in Ihr Projekt zu kopieren und eine beliebige Verknüpfung zu Mapi32. lib und Code zu entfernen, der explizit mit MAPI verknüpft ist.
  
Informationen zum Zugreifen auf die MAPI-Stub-Bibliotheksdateien und zum Erstellen und integrieren dieser in Ihr Projekt sowie Fragen zu dieser Bibliothek, beispielsweise wann und warum Sie verwendet werden können, finden Sie in der [MAPI-Stub-Bibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)
- [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md)
- [Installieren von MAPI-Header Dateien](how-to-install-mapi-header-files.md)
- [Auswählen einer bestimmten zu ladenden MAPI-Version](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Bestimmen der zu verwendenden VerknüpfungsMethode](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Verknüpfen einer ausführbaren Datei mit einer DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

