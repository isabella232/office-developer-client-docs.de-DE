---
title: Multithreading und Arbeitsspeicher Konflikte in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in excel, Arbeitsspeicher Konflikte in Excel, Funktionen [Excel 2007], threadsicheren, threadsicheren Funktionen [Excel 2007], lokalen Speicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790563"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading und Arbeitsspeicher Konflikte in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel-Versionen verwenden als Excel 2007 einen einzelnen Thread für alle Arbeitsblatt Berechnungen. Jedoch kann ab Excel 2007, Excel konfiguriert werden von 1 1024 parallelen Threads für die Berechnung des Arbeitsblatts. Auf einem Computer mit mehreren Prozessoren oder mehreren Prozessorkernen ist die Standardanzahl von Threads gleich der Anzahl der Prozessoren oder Kerne. Aus diesem Grund können threadsicheren Zellen oder Zellen, die nur Funktionen enthalten, die Thread-Sicherheit, sind gleichzeitigen Threads, unterliegen der üblichen neuberechnung Logik, die nach ihrer Vorgängerzellen berechnet werden müssen zugewiesen werden.
  
## <a name="thread-safe-functions"></a>Threadsicheren Funktionen

Die meisten integrierten Arbeitsblattfunktionen in Excel 2007 beginnende sind threadsicheren. Sie können auch Schreiben und Registrieren von XLL-Funktionen als threadsicheren wird. Excel verwendet einen Thread (den Hauptthread), um alle Befehle, Thread unsichere Funktionen, **XlAuto** -Funktionen (außer [XlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12**) und COM- und Visual Basic für Applikationen (VBA) Funktionen aufrufen.
  
In denen eine XLL-Funktion ein **XLOPER** oder **XLOPER12** mit **XlbitDLLFree** zurückgibt, verwendet Excel im gleichen Threads, auf dem der Funktionsaufruf erfolgte **XlAutoFree** oder **xlAutoFree12**aufrufen. Die **XlAutoFree** oder **xlAutoFree12** wird vor der nächsten Funktionsaufruf auf diesem Thread aufgerufen. 
  
Für Entwickler, XLL stehen Vorteile für das Erstellen von threadsicheren Funktionen:
  
- Sie ermöglichen Excel auf einem Computer mit mehreren Prozessoren oder mehreren Prozessorkernen optimal.
    
- Öffnen sie die Möglichkeit der Verwendung von Remoteservern wesentlich effizienter als erledigt werden können einen einzelnen Thread verwenden.
    
Angenommen Sie, Sie haben einen Computer mit einem Prozessor, der Verwendung, sagen, *N* Threads konfiguriert wurde. Nehmen Sie an, dass eine Kalkulationstabelle ausgeführt wird, sendet der macht eine große Anzahl von Anrufen an eine XLL-Funktion, das wiederum eine Anforderung für Daten oder für eine Berechnung auf einem Remoteserver oder Cluster-Servern ausgeführt werden. Unterliegen der Topologie Abhängigkeits-Gesamtstruktur konnte Excel die Funktion N Zeiten fast gleichzeitig anrufen. Den oder die Server ausreichend fast oder parallel sind, die Neuberechnungszeit der Kalkulationstabelle konnte gesenkt werden soweit wie Faktor 1/N. 
  
Das wichtige Problem beim Schreiben von threadsicheren Funktionen wird Konflikte bei Ressourcen ordnungsgemäß behandelt. Bedeutet dies normalerweise Arbeitsspeicher Konflikte, und es kann in zwei Probleme unterteilt werden:
  
- Wie Sie Speicher zu erstellen, die Sie kennen wird nur von diesem Thread verwendet werden.
    
- Wie Sie sicherstellen, dass gemeinsam genutzten Speicher sicher von mehreren Threads zugegriffen wird.
    
Als erstes kennen sollten, ist welchen Speicher in einer XLL von allen Threads zugegriffen werden kann und was nur vom derzeit ausgeführten Thread zugegriffen werden kann.
  
 **Alle Threads zugreifen können**
  
- Deklariert Variablen, Strukturen und Klasseninstanzen außerhalb des Textes, einer Funktion.
    
- Statische Variablen, die in den Textkörper einer Funktion deklariert.
    
In diesen beiden Fällen wird Arbeitsspeicher reserviert in der DLL Speicherblock erstellt für diese Instanz der DLL festgelegt. Wenn eine andere Anwendungsinstanz geladen wird aus die DLL, ruft eine eigenen Kopie dieses Speichers, so, dass keine Konflikte bei dieser Ressourcen von außerhalb dieser Instanz der DLL vorhanden ist.
  
 **Nur vom aktuellen Thread zugegriffen werden.**
  
- Automatische Variablen Funktion-Codes (einschließlich Funktionsargumente).
    
In diesem Fall wird Arbeitsspeicher auf dem Stapel für jede Instanz des Funktionsaufrufs reserviert.
  
> [!NOTE]
> Die dynamisch reservierter Speicher hängen von des Bereichs des Zeigers, das darauf zeigt: Wenn der Mauszeiger von allen Threads zugegriffen werden kann, ist auch der Arbeitsspeicher. Wenn der Zeiger einer automatischen Variablen in einer Funktion ist, ist reservierte Speicher effektiv zu diesem Thread privat. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Arbeitsspeicher, die nur von einem Thread zugegriffen werden: Thread-Local-Speicher

Wenn die statische Variablen in den Textkörper einer Funktion von allen Threads zugegriffen werden kann, sind Funktionen, die sie verwenden deutlich nicht threadsicheren. Eine Instanz der Funktion in einem Thread könnten den Wert ändern, während eine andere Instanz auf einem anderen Thread vorausgesetzt wird, dass sie eine vollständig andere ist. 
  
Es gibt zwei Gründe für das Deklarieren statischer Variables in einer Funktion:
  
1. Statische Daten aus einen Anruf an das nächste beibehalten werden.
    
2. Ein Zeiger auf statische Daten kann problemlos von der Funktion zurückgegeben werden soll.
    
Im Fall von erste Grund sollten Daten enthalten, die beibehalten und ist für alle Anrufe an die Funktion Bedeutung: vielleicht einen einfachen Indikator, der jedes Mal, wenn die Funktion für jeden Thread aufgerufen wird, oder eine Struktur, die Verwendung und Leistungsdaten Eve erfasst Ry Anruf. Die Frage wird der freigegebene Daten oder die Datenstruktur schützen. Dies geschieht am besten mithilfe von kritischen Abschnitt wie im nächste Abschnitt erläutert wird.
  
Wenn die Daten nur für die Verwendung von diesem Thread die könnte die Groß-/Kleinschreibung Grund 1 und ist immer der Fall Grund 2 vorgesehen ist, ist die Frage wie Speicher zu erstellen, die weiterhin auftritt, aber kann nur von diesem Thread zugegriffen werden. Eine Lösung besteht darin, den lokalen Speicher (TLS) API verwenden.
  
Beispiel: haben Sie eine Funktion, die einen Zeiger auf eine **XLOPER**zurückgibt.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Diese Funktion ist nicht threadsicheren, da ein Thread die statische **XLOPER12** zurückgeben kann, während sie einen anderen überschreibt. Die Wahrscheinlichkeit hierfür ist noch größer, wenn die **XLOPER12** an **xlAutoFree12**übergeben werden muss. Eine Lösung besteht darin, eine **XLOPER12**zuweisen, einen Zeiger zu ihm zurückkehren und **xlAutoFree12** implementieren, sodass der **XLOPER12** Speicher selbst freigegeben ist. Dieser Ansatz ist in viele Funktionen Beispiel gezeigt in [Speicherverwaltung in Excel](memory-management-in-excel.md)verwendet.
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Dieser Ansatz ist einfacher zu implementieren als die Vorgehensweise im nächsten Abschnitt werden die TLS-API verwendet, aber es einige Nachteile hat. Excel müssen Sie zunächst **XlAutoFree**Aufrufen/ **xlAutoFree12** aufbauen, den Typ des der zurückgegebenen **XLOPER**/ **XLOPER12**. Zweitens besteht ein Problem bei der Rückgabe **XLOPER**/ **XLOPER12**s, die den Rückgabewert eines Anrufs an eine C-API-Callback-Funktion sind. Die **XLOPER**/ **XLOPER12** möglicherweise zeigen Sie auf Speicher, die durch Excel, aber die **XLOPER**freigegeben werden muss/ **XLOPER12** selbst freigegeben werden muss, auf die gleiche Weise er zugeordnet wurde. Wenn eine solche ein **XLOPER**/ **XLOPER12** ist als den Rückgabewert eine XLL-Arbeitsblattfunktion verwendet werden soll, es ist keine einfache Möglichkeit, **XlAutoFree**informieren/ **xlAutoFree12** müssen beide Zeiger in geeigneter Weise frei. (Festlegen von **XlbitXLFree** und **XlbitDLLFree** das Problem löst nicht die Behandlung von **XLOPER/XLOPER12s** in Excel mit festgelegt ist nicht definiert und möglicherweise ändern von Version zu Version.) Um dieses Problem zu umgehen, kann XLL tiefe Kopien alle Excel zugewiesenen **XLOPER/XLOPER12s** erstellen, die sie an das Arbeitsblatt zurückgibt. 
  
Eine Lösung, die diese Einschränkungen vermieden werden zu füllen und einer lokalen **XLOPER/XLOPER12**zurückzugeben, ein Ansatz, der diese **XlAutoFree/xlAutoFree12** erfordert gibt den **XLOPER/XLOPER12** Zeiger selbst nicht frei. 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Die nächste Frage ist das Einrichten und Abrufen des Thread-Local-Speichers mit anderen Worten, wie im vorherigen Beispiel die Funktion **get_thread_local_xloper12** implementieren. Dies erfolgt mithilfe der Thread lokalen Speicher (TLS) API. Der erste Schritt besteht darin erhalten einen Index TLS mithilfe von **TlsAlloc**, der letztlich mit **TlsFree**freigegeben werden muss. Beide werden am besten aus **DllMain**durchgeführt.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Nachdem Sie den Index abgerufen haben, besteht der nächste Schritt für jeden Thread einen Block von Arbeitsspeicher zugewiesen werden. In der [Dokumentation zur Entwicklung von Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) empfiehlt auf diese Weise jedes Mal, wenn die **DllMain** Callback-Funktion mit einem **DLL_THREAD_ATTACH** -Ereignis aufgerufen wird, und den Speicher bei jedem **DLL_THREAD_DETACH**. Jedoch würde diese Empfehlung folgen die DLL für nicht für die neuberechnung verwendeten Threads unnötige Arbeit leisten. 
  
In diesem Fall ist es besser mithilfe eine Strategie für das zuordnen auf erste verwenden. Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuordnen möchten. Für den vorherigen Beispielen, die **XLOPERs** oder **XLOPER12s**zurückgeben, die folgenden reicht, aber Sie können eine beliebige Struktur, die Ihren Anforderungen erfüllt erstellen.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Die folgende Funktion ruft einen Zeiger auf die Thread-Local-Instanz oder weist einen solchen ist dies der erste Aufruf.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Nun können Sie sehen, wie der Thread-Local **XLOPER/XLOPER12** Arbeitsspeicher abgerufen wird: zunächst rufen Sie einen Zeiger auf die Instanz des Threads von **TLS_data**, und klicken Sie dann geben Sie einen Zeiger auf die darin enthaltenen, wie folgt **XLOPER/XLOPER12** . 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Die Funktionen **mtr_safe_example_1** und **mtr_safe_example_2** können als threadsicheren Arbeitsblattfunktionen registriert werden beim Ausführen von Excel. Sie können nicht jedoch die beiden Methoden in einer XLL verwenden. Ihre XLL kann nur eine Implementierung der **XlAutoFree** und **xlAutoFree12**exportieren, und jeder Strategie Arbeitsspeicher erfordert einen anderen Ansatz. Mit **mtr_safe_example_1**muss der Zeiger übergeben **XlAutoFree/xlAutoFree12** zusammen mit den Daten, die sie auf zeigt freigegeben werden. Mit **mtr_safe_example_2**sollten nur die verweist auf Daten freigegeben werden.
  
Windows bietet eine Funktion **GetCurrentThreadId**, die eindeutige systemweite-ID des aktuellen Threads zurückgibt Dadurch wird den Entwickler mit einer anderen Methode, Code Thread sicher zu machen, oder einen Thread Verhalten bestimmter vornehmen.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Arbeitsspeicher, die nur von mehreren Threads zugegriffen werden: kritische Abschnitte

Sie sollten Lese-Schreib-Speicher schützen, die von mehreren Threads mithilfe von kritischen Abschnitten zugegriffen werden kann. Für die einzelnen Einstellungen zum Blockieren des Speichers, den Sie schützen möchten, benötigen Sie einen benannten kritischen Abschnitt. Initialisieren diese während des Anrufs an die Funktion **XlAutoOpen** und freigegeben werden, und legen Sie diese während des Anrufs an die Funktion **XlAutoClose** auf einen Nullwert fest. Sie müssen jedem Zugriff auf den geschützten Block innerhalb eines Paars von Anrufen an **EnterCriticalSection** und **LeaveCriticalSection**enthalten. Nur ein Thread kann jederzeit in den kritischen Abschnitt. Es folgt ein Beispiel der Initialisierung, zur Aufhebung und Verwenden eines Abschnitts **G_csSharedTable**aufgerufen.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Ein anderes, vielleicht sichererer Ansatz zum Schützen eines Blocks von Arbeitsspeicher ist eine Klasse erstellen, die eine eigene **CRITICAL_SECTION** und dessen Konstruktor, Destruktor enthält und Accessormethoden übernehmen, deren Verwendung. Dieser Ansatz bietet den Vorteil, zum Schutz von Objekten, die initialisiert werden können, bevor **XlAutoOpen** ausgeführt wird oder nach dem **XlAutoClose** aufgerufen wird, aber Sie vorsichtig zum Erstellen von zu viele wichtige Abschnitte und das Betriebssystem Gemeinkosten, die dies erstellen würden. 
  
Wenn Sie Code, die Zugriff auf mehr als ein Block mit geschütztem Speicher zur selben Zeit benötigt haben, müssen Sie die Reihenfolge sorgfältig zu prüfen, in der kritische Abschnitte eingegeben und beendet werden. Beispielsweise könnte die folgenden beiden Funktionen einen Deadlock erstellen.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Wenn die erste Funktion in einem Thread **G_csSharedTableA** eingibt, während die zweite in einem anderen Thread **G_csSharedTableB**eingibt, hängen beide Threads. Der richtige Ansatz ist in einer konsistenten Reihenfolge eingeben und wie folgt in umgekehrter Reihenfolge, beenden.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Sofern möglich, ist es besser aus einem Thread Zusammenarbeit Sicht zum Zugriff auf verschiedene Blöcke zu isolieren, wie hier gezeigt.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Besteht die Konkurrenz für eine freigegebene Ressource, wie häufige zugriffsanforderungen kurze, sollten Sie mit den kritischen Abschnitt Möglichkeit dreht. Dies ist eine Technik gestaltet sich die Ressource weniger prozessorintensive warten. Zu diesem Zweck können Sie entweder **InitializeCriticalSectionAndSpinCount** verwenden, bei der Initialisierung der Bereich oder das **SetCriticalSectionSpinCount** einmal zum Festlegen der Anzahl an, wie oft der Thread gewartet werden Ressourcen in einer Schleife initialisiert verfügbar. Der Wait-Vorgang ist teuer, sodass sich drehenden dies vermieden werden, wenn die Ressource in der Zwischenzeit freigegeben wird. Auf einem System Einzelprozessor die Anzahl der Drehfeld effektiv ignoriert, jedoch können Sie diese weiterhin ohne Schaden angeben. Der Speicher Heap-Manager wird ein Drehfeld Count 4000 verwendet. Weitere Informationen zur Verwendung der wichtigen Abschnitte finden Sie unter Windows SDK-Dokumentation. 
  
## <a name="see-also"></a>Siehe auch



[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

