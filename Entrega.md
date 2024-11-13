# Cognify
## Introducción
El proyecto Cognify plantea una nueva perspectiva en la rehabilitación de criminales, utilizando tecnología avanzada para tratar a los delincuentes como pacientes. Este enfoque reduce la dependencia de las cárceles tradicionales mediante la implantación de recuerdos artificiales, lo que permite cumplir sentencias largas en solo minutos. Cognify no solo busca rehabilitar, sino también reimaginar el sistema de justicia penal.

## Objetivos del Proyecto
Rehabilitación Eficiente: Transformar las experiencias de los delincuentes mediante recuerdos artificiales diseñados para fomentar la empatía y el arrepentimiento.
Reducción de Costos: Minimizar los costos asociados con el encarcelamiento tradicional, como la construcción y mantenimiento de prisiones.
Reinserción Social: Permitir una reintegración rápida y efectiva de los criminales rehabilitados a la sociedad.
Innovación en Justicia Penal: Proporcionar una alternativa ética y tecnológica al castigo convencional, centrada en el aprendizaje y la rehabilitación.

## Codigo

using System;
using System.Collections.Generic;

class Delincuente
{
    public int Id { get; set; }
    public string Nombre { get; set; }
    public string Crimen { get; set; }
    public bool OptaPorRehabilitacion { get; set; }
    public string Estado { get; set; }
    public List<string> RecuerdosImplantados { get; set; }

    public Delincuente(int id, string nombre, string crimen, bool optaPorRehabilitacion)
    {
        Id = id;
        Nombre = nombre;
        Crimen = crimen;
        OptaPorRehabilitacion = optaPorRehabilitacion;
        Estado = "En espera"; // Estado inicial
        RecuerdosImplantados = new List<string>();
    }

    public void ElegirRehabilitacion()
    {
        if (OptaPorRehabilitacion)
        {
            Estado = "Rehabilitación seleccionada";
            Console.WriteLine($"{Nombre} ha elegido rehabilitación acelerada.");
        }
        else
        {
            Estado = "Cumplimiento de sentencia tradicional";
            Console.WriteLine($"{Nombre} cumplirá la sentencia tradicional.");
        }
    }

    public void RealizarMapeoCerebral()
    {
        Console.WriteLine("Realizando mapeo cerebral...");
        // Simulamos la identificación de áreas cerebrales clave
        var mapeo = new Dictionary<string, bool>
        {
            {"hipocampo", true},
            {"corteza_prefrontal", true},
            {"amigdala", true}
        };

        Console.WriteLine("Mapeo cerebral completado.");
    }

    public void ImplantarRecuerdos(string gravedadCrimen)
    {
        Console.WriteLine("Implantando recuerdos...");
        var recuerdos = GenerarRecuerdos(gravedadCrimen);
        RecuerdosImplantados.AddRange(recuerdos);
        Estado = "Rehabilitación completada";
        Console.WriteLine($"Recuerdos implantados para {Nombre}. Empatía y arrepentimiento activados.");
    }

    private List<string> GenerarRecuerdos(string gravedadCrimen)
    {
        var recuerdos = new List<string>();
        
        if (gravedadCrimen == "grave")
        {
            recuerdos.Add("Sentimiento

