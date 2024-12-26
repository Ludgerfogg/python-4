# python-4
Python Week 4


def main():
    print("Welcome to the File Read & Write Program!")
    
    input_filename = input("Enter the filename to read from:input.txt ")
    
    try:
        with open(input_filename, 'r') as infile:
            content = infile.read()
            print("\nFile read successfully!")
        modified_content = content.upper()
        output_filename = input("Enter the filename to write the modified content to:output ")
        
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)
        
        print(f"\nContent has been successfully written to '{output_filename}'.")
   
    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
   
    except PermissionError:
        print(f"Error: You do not have permission to access '{input_filename}'.")

    except Exception as e:
        print(f"An unexpected error occurred: {e}")

if __name__ == "__main__":
    main()

