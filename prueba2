graph LR
    %% Nodo Principal
    Main[<b>GDB: Terminal Chevron Yumbo</b><br>Modelo de Almacenamiento Geográfico]

    %% Estilos
    style Main fill:#2c3e50,stroke:#fff,stroke-width:2px,color:#fff
    style Vec fill:#e1f5fe,stroke:#0277bd,stroke-width:2px
    style Ras fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
    style Alf fill:#fff3e0,stroke:#ef6c00,stroke-width:2px

    %% Conexiones principales (orden: Vectorial – Ráster – Alfanumérico)
    Main --> Vec
    Main --> Ras
    Main --> Alf

    %% ================= VECTORIAL (IZQUIERDA) =================
    subgraph SG_VEC[<b>INFORMACIÓN VECTORIAL</b><br>Feature Datasets]
    direction TB

        Vec[Conjuntos de entidades]

        %% Cartografía base (de lo más general a lo más detallado)
        Vec --> V_Admin[<b>Cartografía Base</b>]
        V_Admin --> V3[Límites Municipales]
        V_Admin --> V1[Veredas]
        V_Admin --> V2[Manzanas Urbanas]
        V_Admin --> V4[Nomenclatura Vial]

        %% Físico / Hidrología
        Vec --> V_Fisico[<b>Físico / Hidrología</b>]
        V_Fisico --> V7[Curvas de Nivel]
        V_Fisico --> V5[Red Hídrica]
        V_Fisico --> V6[Cuerpos de Agua]

        %% Infraestructura
        Vec --> V_Infra[<b>Infraestructura</b>]
        V_Infra --> V8[Construcciones]
        V_Infra --> V9[Polígono Chevron Petroleum]

        %% Gestión y zonificación
        Vec --> V_Gestion[<b>Gestión y Zonificación</b>]
        V_Gestion --> V10[Zona de Estudio]
        V_Gestion --> V11[Área de Influencia]

    end

    %% ================= RÁSTER (CENTRO) =================
    subgraph SG_RAS[<b>INFORMACIÓN RÁSTER</b><br>Imágenes y Superficies]
    direction TB

        Ras[Capas ráster]

        %% Insumos base
        Ras --> R_Insumos[<b>Insumos Base</b>]
        R_Insumos --> R1[DEM - Modelo de Elevación]
        R_Insumos --> R2[Imágenes Satelitales<br>Multitemporales T1 y T2]

        %% Productos derivados
        Ras --> R_Procesos[<b>Productos Derivados</b>]
        R_Procesos --> R3[Índice NDVI]
        R_Procesos --> R4[Clasificación Supervisada<br>Cobertura CLC]

    end

    %% ================= ALFANUMÉRICA (DERECHA) =================
    subgraph SG_ALF[<b>INFORMACIÓN ALFANUMÉRICA</b><br>Tablas y Metadatos]
    direction TB

        Alf[Información tabular]

        %% Nodo “espaciador” invisible para separar del título
        Gap[ ]:::gap

        Alf --> Gap
        Gap --> A1[Tablas de Atributos]
        Gap --> A2[Metadatos ISO 19115<br>Perfil LAMP]

    end

    %% Clase para el nodo espaciador (sin relleno ni borde)
    classDef gap fill:none,stroke:none;
